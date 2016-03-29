##响应式web设计
1.问题的提出：手机浏览器会将一个标准网页缩小至与设备可视区恰好匹配，然后用户在自己感兴趣的内容区域放大浏览。为了看清楚内容，需要不停放大缩小页面，还可以不小心点到了链接
2.H5化繁为简
* 标准的HTML4.01网页文档类型声明如下
> <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" 
"http://www.w3.org/TR/html4/loose.dtd">
H5为
> <!DOCTYPE html>
* HTML4.01链接脚本正确方法为
> <script src="js/jquery.js" type="text/javascript"></script>
H5为
<script src="js/jquery.jss"></script>

3.H5语义化
搜索引擎可以更好理解我们的网页，并评定里面的内容。

4.CS3不破坏任何东西：在老版本浏览器中使用他们无法解析的属性，不会造成任何问题，会欣然忽略无法解析的属性，使我们可以对先进的浏览器进行渐进增强，为老版本浏览器提供合理的降级处理。

5.媒体查询语法，语法很多，列举较常用的。
* css样式表中使用媒体查询
<p><code>
@media screen and (max-width: 960px){
	
}
</code></p>
* 样式表，询问是否为一块纵向放置的显示屏，进而加载portrait-screen.css
<p><code>
	<link rel="stylesheet" media="screen and (orientation : portrait)" href="portrait-screen.css"/>
</code></p>
非纵向放置的屏幕
<p><code>
	<link rel="stylesheet" media="not screen and (orientation : portrait)" href="portrait-screen.css"/>
</code></p>

* 设置视口宽度大于800px才加载文件

<p><code>
	<link rel="stylesheet" media="screen and (orientation : portrait) and (min-width:800px)" href="800wide-portrait-screen.css"/>
</code></p>

* 建议在已有的样式表加入媒体查询，而不是使用@import url("...") screen and ....;因为在ie8以及低版本不支持@import，增加了http请求数量。

6.meta标签可以设置具体的宽度或缩放比例
* <p><code>
	<meta name="viewport" content="initial-scale=1.0,width=device-width"/>
</code></p>
*  设置缩放范围
<p><code>
	<meta name="viewport" content="initial-scale=1.0,maximum-scale=3.0,minimum-scale=0.5,width=device-width"/>
</code></p>
* 禁止缩放
 <p><code>
	<meta name="viewport" content="initial-scale=1.0,user-scalable=no,width=device-width"/>
</code></p>



7.流式布局




