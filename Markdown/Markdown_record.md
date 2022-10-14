**该文档只是up对[Markdown 官方教程](https://markdown.com.cn/basic-syntax/)的个人练习，仅记录up的学习历程，更多内容建议自行搜索**

# 基本语法

## Markdown 基本语法

## Markdown 标题语法

## Markdown 段落语法

我确实喜欢用markdown

我认为从现在开始我会用它格式化我所有的文档

## Markdown 换行语法

可以用两个空格再按回车实现换行----未能实现

也可以使用HTML语法<br>像这样<br>就不用回车了
`Shift`+`Enter`也可以换行

## Markdown强调语法

### 粗体

这里**加粗**，具体方式是在想加粗的部分两边分别加**

### 斜体

这里*倾斜*，具体方式是在想加粗的部分两边分别加*

### 粗体+斜体

这里***粗体+斜体***，具体方式是在想加粗+倾斜的部分两边分别加***

## Markdown引用语法

> 这里引用

具体做法是在开头加>

> 引用里也可以空行
>
> 
>
> 在一个引用框里写完话在回车就行
>
> > 再次输入**>**还可以嵌套引用
> >
> > > ***里面也能加粗***

## Markdown列表语法

1. 可以列表，数字+.+空格

> 1. 一
>
> 2. > two
>    >
>    > > 3. three

2. 也可以嵌套

   1. 像这样

      1. 删除数字再重写就可以了

      - 也可以用点

- 也可以用点

- 只需要用- 开头就可以

  - 分级也是可以的

    - 需要先删除上一级的点

      就可以保持缩进继续书写

- - - - 否则会变成这样

  - 利用***Tab***和***Shift+Tab***可以快速调整层级

    > 引用也是可以的
    >
    > - 里面也可以列表

## Markdown 代码语法

### 转义反引号

利用Esc下方的"`"可以将两个反引号中间的内容标记为代码，like this``里面是代码``

利用两个反引号可以防止关联混乱``Use `code`in your Markdown file``

### 代码块

```R
library(gbm)
```

连续输入三个反引号可创建代码块

## Markdown 分割线

输入三个*或者-或者_可实现分割线

---

## Markdown 链接语法

- ```
  这是一个链接 [Kailai_Liu的Gitee](https://gitee.com/kailai-liu)
  ```

这是一个链接 [Kailai_Liu的Gitee](https://gitee.com/kailai-liu)，[显示名称], (对应url)

---

- ```
  这是一个链接 [Kailai_Liu的Gitee](https://gitee.com/kailai-liu "来看看吧")
  ```

这是一个链接 [Kailai_Liu的Gitee](https://gitee.com/kailai-liu "来看看吧")，鼠标悬停时出现了**提示文字**

---

- ```
  <https://gitee.com/kailai-liu>
  <kailailiu@gmail.com>
  ```

https://gitee.com/kailai-liu
<kailailiu@gmail.com>

两侧加尖括号表示链接

---

- ```
  链接也可以加效果
  **[Kailai_Liu的Gitee](https://gitee.com/kailai-liu "来看看吧")**
  [`Gitee`](https://gitee.com/kailai-liu "来看看吧")
  ```

**[Kailai_Liu的Gitee](https://gitee.com/kailai-liu "来看看吧")**
[`Gitee`](https://gitee.com/kailai-liu "来看看吧")

---

- ```
  链接也可以引用
  如[显示的内容][1] <- [1]为链接的标号
  ```

[这是一个链接][1]

[1]: https://gitee.com/kailai-liu	"来看看吧"

链接中建议用%20代替空格[链接](https://gitee.com/kailai%20liu "好东西")

---

**按住Ctrl+鼠标左键可访问**

## Markdown 图片语法

要添加图像，请使用感叹号 (`!`), 然后在方括号增加替代文本，图片链接放在圆括号里，括号里的链接后可增加一个可选的图片标题文本。

插入图片Markdown语法代码：`![图片alt](图片链接 "图片title")`。

```
![这是图片](C:\Users\Dell\Pictures\favicon.ico "LncTarD 2.0")
```

![这是图片](C:\Users\Dell\Pictures\favicon.ico "LncTarD 2.0")



- 图片也可以添加超链接

  ```
  [![这是图片](C:\Users\Dell\Pictures\favicon.ico "LncTarD 2.0")](https://lnctard.bio-database.com/)
  类似给文本的超链接
  更多内容请访问**[LncTarD 2.0](https://lnctard.bio-database.com/ "疾病&机制关联的lncRNA-target regulation数据库")**
  ```

  [![这是图片](C:\Users\Dell\Pictures\favicon.ico "LncTarD 2.0")](https://lnctard.bio-database.com/)

  更多内容请访问**[LncTarD 2.0](https://lnctard.bio-database.com/ "疾病&机制关联的lncRNA-target regulation数据库")**

# 拓展语法

## Markdown 表格

要添加表，请使用三个或多个连字符 (` --- `) 创建每列的标题，并使用管道 (` | `) 分隔每列。您可以选择在表的任一端添加管道。

```
| ? | ture | false|
就自己填充好了
应该是下面这种
| Syntax | Description |
| --- | ----------- |
| Header | Title |
| Paragraph | Text |
在---左、两边、右加入冒号可实现左对齐，居中，右对齐
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |
```



| ？   | 真                                                | 假   |
| ---- | ------------------------------------------------- | ---- |
| d    | [甚至还可以**添加**链接](www.bing.com "bing搜索") | d    |

```R
library(gbm)
setwd("e:/exp/radiogenomics/")
```

## Markdown 删除线

```
~~我要卷死你们！~~ 还是躺着吧
```

~~我要卷死你们！~~ 还是躺着吧

## Markdown 任务列表

```
- [x] 检查python
- [x] 检查R
- [ ] 提交gitee
```

- [x] 检查python
- [x] 检查R
- [ ] 提交gitee

## Markdown Emoji

Markdown支持Emoji表情，可以通过此**[链接](https://gist.github.com/rxaviers/7360908)**获得Emoji表情代码:blush:

Typora支持Emoji联想，输入冒号+开头字母即可:smile:

~~PS：其实还得搜~~

