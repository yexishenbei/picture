# HTML

### 标签

双标签<marquee> </marquee>

单标签<input>

标签属性：<marquee loop="1"> </marquee>//循环一次

<input type="password">

标题<h1></h1>—<h6></h6>

段落<p></p>

块级元素，无语义<div></div>

常见的语义化标签：

```html
<header></header>  头部
<nav></nav>  导航栏
<section></section>  区块（有语义化的div）
<main></main>  主要区域
<article></article>  主要内容
<aside></aside>  侧边栏
<footer></footer>  底部
```

#### 说说对 html 语义化的理解

HTML标签的语义化，简单来说，就是用正确的标签做正确的事情，给某块内容用上一个最恰当最合适的标签，使页面有良好的结构，页面元素有含义，无论是谁都能看懂这块内容是什么。

语义化的优点如下：

- 在没有CSS样式情况下也能够让页面呈现出清晰的结构
- 有利于SEO和搜索引擎建立良好的沟通，有助于爬虫抓取更多的有效信息，爬虫是依赖于标签来确定上下文和各个关键字的权重
- 方便团队开发和维护，语义化更具可读性，遵循W3C标准的团队都遵循这个标准，可以减少差异化



#### `Doctype`是HTML5的文档声明

#### 前端页面有哪三层构成，分别是什么？

构成：`结构层`、`表示层`、`行为层`

1. 结构层（structural layer）

   结构层类似于盖房子需要打地基以及房子的悬梁框架，它是由HTML超文本标记语言来创建的，也就是页面中的各种标签，在结构层中保存了用户可以看到的所有内容，比如说：一段文字、一张图片、一段视频等等

2. 表示层（presentation layer）

   表示层是由CSS负责创建，它的作用是如何显示有关内容，学名：`层叠样式表`，也就相当于装修房子，看你要什么风格的，田园的、中式的、地中海的，总之CSS都能办妥

3. 行为层（behaviorlayer）

   行为层表示网页内容跟用户之间产生交互性，简单来说就是用户操作了网页，网页给用户一个反馈，这是`JavaScript`和`DOM`主宰的领域

#### 行级元素和块级元素分别有哪些及怎么转换？

- 1. 块级元素 (Block-level elements)

  - **定义**：块级元素通常会占据一整行，并且其后的内容会从新的一行开始显示。它们的宽度通常会自动填满父容器的宽度。
  - **常见块级元素**：
    - `<div>`
    - `<p>`
    - `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`
    - `<ul>`, `<ol>`, `<li>`无序列表,有序列表,列表项
    - `<header>`, `<footer>`, `<section>`, `<article>`, `<nav>`
    - `<form>`, `<fieldset>`, `<table>`
  - **特点**：
    - 它们会在页面上显示为独立的块状区域。
    - 可以设置宽度和高度。
    - 默认情况下会从新的一行开始。

  2. 行内元素 (Inline elements)

  - **定义**：行内元素只占据它自身所需要的宽度，不会导致页面换行。它们与其他行内元素在同一行内显示。
  - **常见行内元素**：
    - `<span>`
    - `<a>`创建超链接<a href="https://www.example.com"></a>
    - `<strong>`, `<em>`加粗，斜体
    - `<img>`
    - `<b>`, `<i>`加粗，斜体
    - `<br>`, `<code>`自闭合标签，用于插入换行符；显示计算机代码
  - **特点**：
    - 不会导致换行，通常是文本的一部分。
    - 无法设置宽度和高度，通常只使用文本的实际内容大小。
    - 只能在父元素的宽度内排列。

如何转换（块级和行内的转换）

有时你可能需要改变元素的默认显示行为，这可以通过 CSS 来实现。可以使用 `display` 属性来转换元素的显示类型：

- **块级元素转为行内元素**：

  ```
  css复制编辑.my-block {
      display: inline;
  }
  ```

  这样，`.my-block` 原本是块级元素，它将被转为行内元素。

- **行内元素转为块级元素**：

  ```
  css复制编辑.my-inline {
      display: block;
  }
  ```

  这样，`.my-inline` 原本是行内元素，它将被转为块级元素。

- **行内块元素（既有行内性质，也有块级性质）**：

  ```
  css复制编辑.my-inline-block {
      display: inline-block;
  }
  ```

  `inline-block` 让元素既能够并排显示，又可以像块级元素一样设置宽度和高度。

![image-20250217202118577](C:\Users\vence\AppData\Roaming\Typora\typora-user-images\image-20250217202118577.png)

图片标签

`<img`

​	`src="/img/1.jpg?param=300x300"`图像源

​	`	alt="封面"`图像描述

`/>`



#### 跳转到锚点

![image-20250217191954673](C:\Users\vence\AppData\Roaming\Typora\typora-user-images\image-20250217191954673.png)

![image-20250217192310429](C:\Users\vence\AppData\Roaming\Typora\typora-user-images\image-20250217192310429.png)

#### 唤起指定应用

![image-20250217193040377](C:\Users\vence\AppData\Roaming\Typora\typora-user-images\image-20250217193040377.png)

#### 列表

ol有序,ul无序,dl定义。`<li>`：表示列表项，写在ul,ol里

![image-20250217195705819](C:\Users\vence\AppData\Roaming\Typora\typora-user-images\image-20250217195705819.png)

dl中的**标签**：

- `<dl>`：用于定义整个定义列表。
- `<dt>`：定义术语（Definition Term）。
- `<dd>`：定义术语的解释或描述（Definition Description）

#### 表格

![image-20250217201202035](C:\Users\vence\AppData\Roaming\Typora\typora-user-images\image-20250217201202035.png)

#### 表单

交互区域，主要用于收集用户数据

![image-20250217202949984](C:\Users\vence\AppData\Roaming\Typora\typora-user-images\image-20250217202949984.png)

![image-20250217203456350](C:\Users\vence\AppData\Roaming\Typora\typora-user-images\image-20250217203456350.png)

单选框和复选框要写value

![image-20250217204205545](C:\Users\vence\AppData\Roaming\Typora\typora-user-images\image-20250217204205545.png)

隐藏域 type="hidden"

#### 框架标签

<i/f/r/ame src=”“></iframe>//嵌入网页

![image-20250217210415811](C:\Users\vence\AppData\Roaming\Typora\typora-user-images\image-20250217210415811.png)

![image-20250217210625732](C:\Users\vence\AppData\Roaming\Typora\typora-user-images\image-20250217210625732.png)

# CSS

![image-20250217212421020](C:\Users\vence\AppData\Roaming\Typora\typora-user-images\image-20250217212421020.png)

外部标签，在html文件中引入css：（8，9行）

![image-20250217212818717](C:\Users\vence\AppData\Roaming\Typora\typora-user-images\image-20250217212818717.png)

#### 样式

主要用外部样式

![image-20250217214354649](C:\Users\vence\AppData\Roaming\Typora\typora-user-images\image-20250217214354649.png)