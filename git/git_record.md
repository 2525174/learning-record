该内容根据 bilibili UP **遇见狂神说** 相关视频记录学习，视频戳[这里](https://www.bilibili.com/video/BV1FE411P7B3/?spm_id_from=333.999.0.0&vd_source=9133539af302d5d54446b467fe568b43)

# git 相关知识

## 为什么选择git

选择git是为了**版本控制**, 便于查看每个版本的代码改动, 每个人都可以从远程仓库获得所有的代码

SVM每个人只能上传, 普通人看不到所有的代码

git由Linux之父用两星期开发完成, 最初是为了Linux的开发而设计的

**git是最好最先进的版本控制软件!!!**

## 环境配置

`git config -l` 	`-l ` 表示”list“，列出清单——列出git的配置信息

`git config --system -l`	`--system` 表示筛选system的配置

`git config --blobal -l` 	看自己的配置文件

​	`git config --blobal user.name "自己的用户名"`	

​	`git config --global user.email "自己的email@example.com"`

git配置文件存放地址

| file   | file path                |
| ------ | ------------------------ |
| system | git\etc\gitconfig        |
| global | C:\users\Dell\.gitconfig |

.开头的文件需要查看隐藏文件

## git的四个工作区

git有四个工作区: 工作目录 work directory, 暂存区 stage(index), 本地git库 repository, 远程git库 remote directory

![git四个工作区](C:\Users\Dell\AppData\Roaming\Typora\typora-user-images\image-20221014203748331.png)

- **工作区 Workspace**: 放代码的地方
- **暂存区 Stage (Index)**: 临时存放改动, 只是一个文件
- **仓库区 Repository**: 安全存放数据的位置, 所有版本的数据都在这里. HEAD指向最新放入的版本. ~~目前只涉及到主分支, 更多分支 (如开发分支) 未学习~~
- **远程仓库 Remote Repository**: 托管代码的服务器, 如 github, gitee. 企业还可以设置gitlab来实现内部的使用

## git实战

### 新建git项目

新建git项目有两种方式:

1. 新建git项目`git init` 
2. 克隆已有项目`git clone url`. 此处的url从github的仓库获取

### 查看文件状态

`git statue` 查看文件状态

- `untracked` 表示文件未跟踪, 未进行版本控制, 需要使用 `git add .`将文件添加到暂存区
- `committed` 表示文件在暂存区, 需要用`git commit -m '新增..., 修改...'` 提交文件至仓库区. 也可在弹出的编辑器内更改提交记录,  删除"#", `Ctrl+S`, 关闭窗口即可

工作区存在大量数据无需进行版本控制, 建立 `.gitignore` 文件忽略相关内容

| 命令     | 操作                      |
| -------- | ------------------------- |
| *.txt    | 忽略所有后缀名为txt的文件 |
| !lib.txt | 但lib.txt除外             |
| build/   | 忽略build文件夹           |
| /temp    | 忽略包含temp的文件夹      |

### push到远程仓库

首先注册账号 (github, gitee), 配置ssh

- `C:\users\Dell\.ssh` 文件夹下 (没有的话新建一个) , 右键新建git bash窗口, 输入`ssh-keygen -t rsa` rsa表示加密算法. 输入完成后一直回车下一步即可
- 该文件夹下会有两个文件, `id_rsa` 为私钥, `id_rsa.pub`为公钥, 去远程代码库输入公钥下的文本即可连接
- 首先在远程代码库建立仓库, 使用 `git push -u origin "master"` 将本地仓库同步到远程仓库
  *!!!此处可能会有邮箱不匹配的问题, 可以去gitee设置页面选择公开邮箱地址, 也可以用`git config --global user.email "fakeemail@example.com"` 将本地配置更改为gitee的假邮箱*
- 配置结束, 可每次使用 `git push` 将本地仓库推送到远程仓库

### 利用vscode同步git

安装vscode及git插件, 自己研究研究就会了...