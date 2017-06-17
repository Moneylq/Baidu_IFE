### 任务目的
- 通过实现一个常见的技术产品官网，加深对于HTML，CSS的实战能力
- 学习掌握如何在没有标注的情况下实现设计稿到页面的精确转变
### 任务描述
- 通过HTML及CSS实现设计稿,效果如 [效果图（点击打开）](http://7xrp04.com1.z0.glb.clouddn.com/task_1_7_2.jpg)
- 设计稿是有一定宽度的，这个宽度为页面的最小宽度，也就是说，当浏览器窗口宽度小于设计稿宽度时，允许出现横向滚动条，页面内容宽度保持不变，但是当浏览器窗口宽度大于设计稿宽度时，页面部分内容的宽度应该保持和浏览器窗口宽度一致。
### 任务注意事项
- 只需要完成```HTML```，```CSS```代码编写，不需要写```JavaScript```
- 设计稿中的图片、文案均可自行设定
- 在```Chrome```中完美实现与设计稿的各项字体、布局、内外边距等样式



##### 页面顶部导航条左右两边的元素使用浮动来使元素分别显示在左右两边
##### 有一列无需列表，除了最后一项都加了下边框，应使用```li:last-child:{border-bottom:none}```
```
<style type="text/css">
		ul {
			cursor: pointer;
		}
		ul li {
			float: left;
			margin-right: 20px;
			list-style: none;
		}
		ul li a {
			text-decoration: none;
		}
		ul li:hover {
			border-bottom: 4px solid red;
		}
		ul li:hover a {
			color: red;
		}
		ul li:last-child:hover {
			border-bottom: none;
		}
	</style>
</head>
<body>
	<ul>
		<li><a href="#">aa</a></li>
		<li><a href="#">bb</a></li>
		<li><a href="#">cc</a></li>
		<li><a href="#">dd</a></li>
		<li><a href="#">ee</a></li>
		<li><a href="#">ff</a></li>
	</ul>
</body>
```
##### ```transition```属性，鼠标移入渐变效果
```
<style type="text/css">
			.test {
				width: 1000px;
				height: 100px;
				text-align: center;
			}
			
			.test p {
				cursor: pointer;
			}
			
			.test span {
				width: 20px;
				height: 10px;
				display: inline-block;
				border-bottom: 5px solid red;
				transition: width 1.5s;
				-moz-transition: width 1.5s;
				/* Firefox 4 */
				-webkit-transition: width 1.5s;
				/* Safari 和 Chrome */
				-o-transition: width 1.5s;
				/* Opera */
			}
			
			.test p:hover~span {
				width: 200px;
			}
		</style>
	</head>

	<body>
		<div class="test">
			<p>测试鼠标移入渐变效果</p>
			<span></span>
		</div>
	</body>
```
##### 总结：还有一点没完成，就是带三角形的边框，这个，没搞好，回头搞明白了再补上。
