# 第一次任务

*以后文件编辑完了一定记得保存，呜呜呜，借鉴学姐的答案把自己的完善的第二遍，自我赶集还8错*

# 1.内联标签（元素）和块级标签（元素）的区别

1.1块级元素一般用来搭建网站大的框架，布局，例如：div，ul，ol，li，dd，dt，dl，h1～h6，p，block元素默认独占一行，后面无论紧跟什么元素，都会另起一行；block元素的默认宽度是父元素的100%，可以设置高与宽，以及padding值与margin值；width设置为100%的优点就是说它会根据浏览器的变化而自己调整宽度。

*常见块级元素*

```
<div></div> 
<dd></dd><dl></dl>
<form></form>
<hr>
<header></header>
<h1>-<h6>
<ol></ol>
<p></p>
<table></table>
<ul></ul>
```

1.2 内联元素主要是为了具体设计某几个字的样式而存在的。inline元素不会独占一行，始终是从左往右排列，排不下的话才会另起一行，inline元素的宽度的跟随内容自动撑起来的，内容有多长，宽度就是多宽

*常见行内元素*

~~~
<a></a> 
<abbr></abbr> 
<em></em>
<strong></strong>
<span></span>
<br> 
<img>
<script></script>
<label></label>
~~~



1.3 block element 与inline element 之间可以相互转化，通过display

补充学姐提醒

1.3内联块级元素

- 一个内联块级元素同时具备内联元素、块级元素的特点

- 文档流方向为从左到右

- 元素的高度、宽度、行高以及顶和底边距都可设置

- 相当于是添加了左浮动

  *常见的内联块级元素*

  - ```
    <button></button>
    <input>
    <textarea></textarea>
    ```



# 2. input标签至少五种不同的type及应用

2.1 type=text，输入类型是text，比如登陆输入用户名，注册输入电话号码，电子邮件，家庭住址等等，是Input的默认类型。

2.2 type=password，当在此输入框输入信息时显示为保密字符

2.3 type=file，提供了一个文件目录输入的平台，参数有name，size。

2.4 type=button，就是按钮

2.5 type=checkbox，复选框

2.6 type=radio,单选按钮

*举个梨子*

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>type</title>
    </head>
    <body>
    <p>文本/密码：</p>
    <form>
        id:<input type="text" name="id">
        <br/>
        password:<input type="password" name="password">
    </form>
    <p>单选type=radio：</p>
    <form>
        <input type="radio" name="sex" value="boy">boy
        <br/>
        <input type="radio" name="sex" value="girl">girl
    </form>
    <p>复选type=checkbox：</p>
    <form>
        <input type="checkbox" name="fruit" value="apple">apple<br/>
        <input type="checkbox" neme="fruit" value="banana">banana<br/>
        <input type="checkbox" name="fruit" value="chery">chery<br/>
    </form>
    <p>提交按钮：</p>
    <form>
        <input type="submit" name="user">
    </form>
    </body>
</html>
```



# 3. table标签中tr th td的含义

3.1 tr表格的行标签

3.2 th表头单元格（文字加粗）

3.3 td单元格

*再举个栗子*

```<!DOCTYPE html>
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>type</title>
    </head>
    <table border="1">
    <tr>
        <th></th>
        <th>Monday</th>
        <th>Tuesday</th>
        <th>Wednesday</th>
        <th>Thursday</th>
        <th>Friday</th>
    </tr>
    <tr>
        <th>8:00-10:10</th>
    </tr>
    <tr>
        <th>10:30-12:10</th>
    </tr>
    </table>
</html>
```

# 4. img标签和a标签分别是如何实现链接的

4.1 img通过src属性

`<img src="" alt="".../>`

4.2 a通过href属性

`<a href="" >xxx</a>`

# 5. CSS选择器的优先级

5.1 在属性后面使用!important会覆盖页面内任何位置定义的元素样式。

5.2 作为style属性写在元素内的样式

5.3 id选择器

5.4 类选择器

5.5 标签选择器

5.6 通配符选择器

5.7 浏览器自定义或继承

# 6.盒模型

盒模型是CSS中一个重要概念，文档中的每个元素被描绘为矩形盒子。渲染引擎的目的就是判定大小，属性。盒模型属性有：

margin：外边距

padding：内边距

border：边框

content：内容

[盒模型](https://www.cnblogs.com/chengzp/p/cssbox.html)

# 7.绝对定位、相对定位和fixed定位

7.1 absolute定位：绝对定位的元素的位置相对于最近的已定位父元素，如果元素没有已定位的父元素，那么它的位置相对于<html>

7.2 relatibe定位：相对定位元素的定位是相对其正常位置

7.3 fixed定位：元素的位置相对于浏览器窗口是固定位置。即使窗口是滚动的它也不会移动：

[分享篇大佬的博客](https://www.cnblogs.com/heroine/p/5852748.html)

# 8.浮动

CSS float 属性定义元素在哪个方向浮动，浮动元素会生成一个块级框，直到该块级框的外边缘碰到包含框或者其他的浮动框为止。CSS 的 Float（浮动），会使元素向左或向右移动，其周围的元素也会重新排列。

[向前辈学习](https://blog.csdn.net/nanjinzhu/article/details/82716522)

# 9.如何链接外部css文件

<head><link rel="stylesheet" type="text/css" href="mystyle.css"></head>

# 10. F12调试工具怎么用

简单的讲，就是按下键盘的F12键（一本正经）

9.1元素（Elements）：

Ctrl+Shift+C进入选择元素模式，然后从页面中选择需要查看的元素，然后可以在开发者工具元素（Elements）一栏中定位到该元素源代码的具体位置 

查看元素属性：可从被定位的源码中查看部分，如class、src，也可在右边的侧栏中查看全部的属性，如下图位置查看

修改元素的代码与属性：可直接双击想要修改的部分，然后就进行修改，或者选中要修改部分后点击右键进行修改9.2 控制台（Console）：

控制台一般用于执行一次性代码，查看JavaScript对象，查看调试日志信息或异常信息。

9.3 源代码（Sources）：

该页面用于查看页面的HTML文件源代码、JavaScript源代码、CSS源代码，此外最重要的是可以调试JavaScript源代码，可以给JS代码添加断点等。

9.4 网络（Network）：

网络页面主要用于查看header等与网络连接相关的信息

一共分为四个模块：

Header：面板列出资源的请求url、HTTP方法、响应状态码、请求头和响应头及它们各自的值、请求参数等等

Preview：预览面板，用于资源的预览。

Response：响应信息面板包含资源还未进行格式处理的内容

Timing：资源请求的详细信息花费时间

