# learninghtml
记录一下学习HTML过程中编写的代码
里面的文字内容大部分都是抄的教程用于记笔记



## HTML 简介

### 什么是HTML

HTML 是用来描述网页的一种语言
* HTML全称为 Hyper Text Markup Language
* HTML 不是一种编程语言，而是一种标记语言
* 标记语言是一套**标记标签**(markup tag)
* HTML 使用标记标签来描述网页
* HTML 文档包含了 HTML 标签及 **文本** 内容
* HTML 文档也叫做 **WEB** 页面



### HTML 标签

HTML 标记标签通常被称为 HTML 标签（HTML tag)

* HTML 标签是由尖括号包围的关键词，比如 `<html>`
* HTML 标签通常是 *成对出现* 的，比如 `<b>` 和 `</b>`
* 标签对中的第一个标签是 *开始标签*，第二个标签是 *结束标签*
* 开始和结束也被称为 *开放标签*  和 *闭合标签*

```HTML
<标签>内容</标签>
```



### HTML 元素

HTML 标签 和 HTML 元素通常都是描述同样的意思

但是严格来讲，一个HTML元素包含了开始标签和结束标签，如以下示例：

```html
<p>
    这是一个段落
</p>
```



### WEB 浏览器

Web 浏览器 是用于读取 HTML 文件，并将其作为网页显示。

浏览器并不是直接显示的HTML标签，但是可以使用标签来决定如何展现HTML 页面的内容给用户

> 只有 `<body>` 区域才会在浏览器中显示。



### `<!DOCTYPE>` 声明

`<!DOCTYPE>` 声明有助于浏览器中正确显示网页

网络上有很多不同的文件，如果能够正确声明HTML的版本，浏览器就能正确显示网页内容。

DOCTYPE 声明是不区分大小写的，以下方式均可：

```html
<!DOCTYPE html>
<!DOCTYPE HTML>
<!doctype html>
<!DocType Html>
```

DOCTYPE标签是一种标准的用标记语言的文档类型声明，它的目的是要告诉标准通用标记语言解析器，它应该使用什么样的文档类型定义(DTD)来解析文档。

`<!DOCTYPE>` 声明必须是HTML文档的第一行，位于 `<html>` 标签之前

**作用**：声明文档的解析类型，避免浏览器的怪异模式

浏览器有两种声明模式，一种是 `BackCompat`：怪异模式，浏览器使用自己的怪异模式解析渲染画面

一种是`CSS1Compat`：标准模式，浏览器使用W3C的标准解析渲染页面

这个属性会被浏览器识别并使用，如果页面中没有`<!DOCTYPE>` 的声明，那么compatMode默认就是怪异模式，浏览器按照自己的方式解析页面，那么在不同的浏览器中，会显示不同的样式；如果添加了`<!DOCYTPE html>` 那么就等同于开启了标准模式。那么浏览器将按照W3C的标准解析渲染页面。



### 中文编码

在大部分浏览器中，直接输出中文会出现中文乱码的情况，这时候我们就需要在头部将字符声明为UTF-8 或 GBK。

```html
<!-- <!DOCTYPE html> 声明为 HTML5 文档 -->
<!DOCTYPE html>

<!-- <html> 元素是 HTML 页面的根元素 -->
<html>

<!-- <head> 元素包含了文档的元(meta)数据，如<meta charset="utf-8"> 定义网页编码格式为UTF-8 -->

<head>
    <meta charset="utf-8">
    <!-- <title>元素描述了文档的标题 -->
    <title>Yves的第一天html之旅</title>
</head>

<!-- <body> 元素包含了可见的页面内容 -->

<body>
    <!-- <h1>元素定义一个大标题 -->
    <h1>我的第一个标题</h1>
    <!-- <p>元素定义一个段落 -->
    <p>我的第一个段落</p>
</body>

</html>
```



## HTML 基础

### HTML 标题
HTML 标题(heading) 是通过`<h1> - <h6>` 来定义的



### HTML 段落
HTML 段落是通过标签`<p>` 来定义的

### HTML 链接
HTML 链接是通过标签 `<a>` 来定义的
**提示**： 在href 属性中指定链接的地址。

### HTML 图像
HTML 图像是通过标签`<img>` 来定义的
**注意**：图像的名称和尺寸是以属性的形式提供的。

### HTML 元素

HTML 文档由HTML元素定义。

## HTML 元素

HTML 文档由 HTML 元素定义。

### HTML 元素

| 开始标签                  | 元素内容     | 结束标签 |
| ------------------------- | ------------ | -------- |
| `<p>`                     | 这是一个段落 | `</p>`   |
| `<a href="default.html">` | 这是一个链接 | `</a>`   |
| `<br>`                    | 换行         |          |

开始标签通常被称为**起始标签(opening tag)**，结束标签通常被称为**闭合标签(closing tag)**



### HTML 元素语法

* HTML 元素以**开始标签**起始
* HTML 元素以**结束标签**终止
* **元素的内容**是开始标签与结束标签之间的内容
* 某些HTML元素具有**空内容（empty content）**
* 空元素**在开始标签中进行关闭**（以开始标签的结束而结束）
* 大多数HTML元素可拥有**属性**



### 嵌套的HTML 元素

大多数HTML元素可以嵌套（HTML 元素可以包含其他HTML元素）。

HTML文档由相互嵌套的HTML元素组成。
