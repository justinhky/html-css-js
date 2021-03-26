# HTML
html is hypertext markup language由欧洲核子研究中心的物理学家蒂姆·伯纳斯-李（Tim Berners-Lee）发明。
它的最大特点是支持超链接，点击链接就可以跳转到其他网页，从而构成整个互联网。  
浏览器的网页开发设计三种技术，HTML，CSS和Javascript。  
- HTML定义网站的结构和内容  
- CSS样式表定义网页的样式  
- Javascript定义网页和用户的互动行为  

## 1. 网页的基本概念
### 1.1 标签  
网页的 HTML 代码由许许多多不同的标签（tag）构成。学习 HTML 语言，就是学习各种标签的用法。  
HTML 语言忽略缩进和换行  
### 1.2 元素  
浏览器渲染网页时，会把 HTML 源码解析成一个标签树，每个标签都是树的一个节点（node）。这种节点就称为网页元素（element）。
所以，“标签”和“元素”基本上是同义词，只是使用的场合不一样：标签是从源码角度来看，元素是从编程角度来看，比如<p>标签对应网页的p元素。  
==嵌套的标签就构成了网页元素的层级关系。==
### 1.3 块级元素，行内元素
### 1.4 属性  
属性不区分大小写，用来定制标签的行为  
## 2. 网页的基本标签  
```
<!DOCTYPE>  
<!DOCTYPE html>
<html>  
<html lang="zh-CN">

<head>  
    <meta>
    <link>
    <title>
    <style>
    <script>
    <noscript>
    <base>  
<meta>  
<meta charset="utf-8">  
<meta name="viewport" content="width=device-width, initial-scale=1">  
```
meta表示元数据，用于设置或者说明网页的元数据，网页可以有多个meta标签，meta标签约定放在head内容的最前面。常见的元数据有keywords, description, author, etc。  
<title>  
<body>  
## 3. 空格和换行  
HTML忽略内容的头部和尾部的空格，会合并内容中间的空格成制表符\t，html还会将文本里面的换行\n和回车\r，替换成空格。  
## 4. 注释  
<!-- words -->注释内容不会显示在网页上，但可以在源代码中查看。  

## 5. URL简介  
url是“统一资源定位符”uniform resource locator"的首字母缩写，中文是网址  
### url的组成部分  
#### 协议scheme  
协议是浏览器请求服务器资源的方法，互联网支持多种协议，必须指明网址使用哪一种协议，默认http协议。其他还有邮件协议**mailto:**后面只有一个冒号  
#### 主机host  
主机就是资源所在的网站名或服务器的名字，又称为域名，比如www.sample.com，有些主机只有ip地址，一般出现在局域网  
#### 端口  
同一个域名下可能包含多个网站，他们之间通过端口区分。端口就是一个整数，简单理解就是访问者告诉服务器，想要访问哪个网站。默认端口80，如果省略了这个参数服务器就返回80端口的网站。  
#### 路径path  
路径就是资源在网站上的位置，比如/path/index.html。路径可能只包含目录，不包含文件名，比如/foo/，甚至结尾的斜杠都可以省略。这时，服务器通常会默认跳转到该目录里面的index.html文件（即等同于请求/foo/index.html）
但也可能有其他的处理（比如列出目录里面的所有文件），这取决于服务器的设置。一般来说，访问www.example.com这个网址，很可能返回的是网页文件www.example.com/index.html。  
#### 查询参数  
查询参数（parameter）是提供给服务器的额外信息。参数的位置是在路径后面，两者之间使用?分隔上例是?key1=value1&key2=value2。  
查询参数可以有一组或多组。每组参数都是键值对（key-value pair）的形式，同时具有键名(key)和键值(value)，它们之间使用等号（=）连接。比如，key1=value就是一个键值对，key1是键名，value1是键值。  
多组参数之间使用&连接，比如key1=value1&key2=value2。  
#### 锚点anchor  
锚点（anchor）是网页内部的定位点，使用#加上锚点名称，放在网址的最后，比如#anchor。浏览器加载页面以后，会自动滚动到锚点所在的位置。  
### url字符
url各个部分只能使用以下字符：  
- 26个英语字母（包括大写和小写）  
- 10个阿拉伯数字  
- 连词号（-）  
- 句点（.）  
- 下划线（_）  
### <base>标签  
<base>标签指定网页内部的所有相对 URL 的计算基准。整张网页只能有一个<base>标签，而且只能放在<head>里面。它是单独使用的标签，没有闭合标签，下面是一个例子。  
<head>  
<base href="https://www.example.com/files/" target="_blank">  
</head>  
注意，<base>标签必须至少具有href属性或target属性之一。一旦设置了<base>，就对整个网页都有效。如果要改变某个链接的行为，只能用绝对链接替代相对链接。
尤其需要注意锚点，这时锚点也是针对<base>计算的，而不是针对当前网页的 URL。  



