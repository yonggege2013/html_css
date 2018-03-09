
注：inhert 代表继承上一个布局

边线 border
内部填充 padding
外部填充 margin
宽度和高度 width height


定义元素外边框 outline   ；是元素的外边框，有别于border,在border之外

text-align:文本内容的位置，靠左，靠右，居中,调整,left,right,center,justify
text-decoration:文本内容的中线，上线，下划线 line-through,overline,underline
text-transform:文字的大小写转换 lowercase（小写）,uppercase（大写）,capitalize(把首字母转化成大写)
text-indent:设置文本内容的缩行 150px
letter-spacing:设置文本内容的字符间隔 normal（默认） 20px -20px（代表缩小间隔）
word-spacing:设置单词之间的间隔 20px
line-height:设置文本内容的行间距 1.5 1.5px

font-family:设置字体的样式cursive,sans-serif,serif(可以放三种字体)
font-style:设置字体的风格 italic(斜体)
font-size:设置字体的大小（默认16px）1em(1em = 16px,浏览器默认字体大小) 注：在body中设置字体大小为100%，然后在子标签中shezhi字体大小为1em，确保兼容不同的浏览器
font-weight:设置字体的粗细100;


display:控制元素的显示状态 none;block(块状显示)，inline(行内元素显示,设置宽高无效),line-block(表现为行内元素，可设置宽高)
visibility:hidden

max-width：最大宽度（margin:auto可以设置左右元素居中）

position:指定元素的位置
static(默认显示)、
relative(相对于元素原来的位置，设置top,left后可使得元素进行移动)。。。。top:相对于上面的位置移动距离。。。。left同理 
fixed(相对于元素原来的位置设置top，left后可使得元素进行移动,和relative不同的是位置不会随滚动条的
滚动而发生位置变化++++++++++++++++++++++++++++++++++++++)
absolute(相对离得近的位置元素)

z-index:出现层叠时，使谁显示在最上层

overflow、overflowX,overflowY:控制元素的溢出，当元素的内容超过元素的宽高后的表现形式 visible(默认) hidder(隐藏) scroll(滚动) auto(自动根据内容处理)


float:控制元素的浮动，使元素脱离整个界面结构。left/right(靠左/右浮动)。若使其他元素不受影响，则其他元素使用clear属性

.clearfix::after

float应用


align:元素的对齐方式
1,元素水平居中：margin:auto
2,文字水平居中：text-align:center
3,图片水平居中:display:block margin:auto
4,通过position设置对齐，左对齐，右对齐
5，垂直居中对齐一、padding
二、 line-height display
三、
position text-align:center
position:absolute
margin:0
top:50%
left:50%
transform:translate(-50%,-50%)


设置元素透明度
opacity:值为0-1
rgba



CSS3的常用部分


设置阴影
box-shadow:15px 15px 10px....虚化效果 grey;

过渡使用
transition
.init {
	width:200px;
	height:200px;
	background-color:lightblue;
	transition:1s linear或ease或ease-in或ease-out或ease-in-out 2s(延迟)
	-webkit-transition:为了兼容，必须加-webkit-
}

.init:hover {//鼠标移上去的状态
	width:800px;
}

设置动画
animation 使用 .aaa{
	animation:example 2s 1s(延迟) ease-in-out infinite reverse....alertnate;
}
@keyframes example {
	<!-- from{background-color:green}
	to{background-color:blue} -->


	0%{background-color:green}
	25%{background-color:blue}
	50%{background-color:green}
	75%{background-color:blue left:80%}
}


CSS选择器 指定规则应用在什么上面

简单选择器 

元素选择器 p h1 h2
类选择器 .p2
id选择器 #p2 id不能重复
优先级：id选择器>类选择器>元素选择器

组合选择器

后代选择器（空格）
子选择器（>）
相邻兄弟选择器（+）
一般兄弟选择器（~）


后代选择器
div p {//代表div中的所有p元素
	
}

子代选择器
div > p {//代表div中的直接子元素p
	
}

相邻兄弟选择器
div + p {//代表div的同一级别的直接相邻的p元素
	
}

一般兄弟选择器
div ~ p {//代表div的同一级别的所有的p元素
	
}

伪类选择器：指一个元素的某个状态的选择器
div {
	
}
div:hover {//鼠标置于div上
	
}

div p:first-child {//div中的后代的第一个p元素
	
}



伪元素选择器：用于选择元素的某一个部分

p::first-line {
	color:red;
}
p::first-letter {
	
}

span::after {
	content:" new !"
	color:red;
}

p::selection {//选中状态
	
}

属性选择器

p[title] {//只要有某个属性
	background-color:yellow;
}

p[title="abc"] {//必须属性等于某个值
	
}

p[title~="a"] {//属性包含某个单词（空格隔开）的，空格隔开的为一个单词的
}

p[title*="ab"] {//属性版包含有某个字符串的
	
}

p[title|="1"] {//属性必须以某个单词（-隔开）开始
	
}

p[title^="ab"] {//属性必须以某个值开始
	
}
p[title$="c"] {//属性必须以某个值结尾
	
}
<!DOCTYPE html>
<html>
<head>
	<title></title>
</head>
<body>
   <p title="abc"></p>
   <p title="1-11"></p>
   <p title="abcd"></p>
   <p title="a bc"></p>

</body>
</html>



Box model
1.content
2.padding
3.border
4.margin


Box Sizing CSS3中的属性值

box-sizing:为了使浏览器在元素宽高相同时表现出相同的大小，去除padding的影响而去设置的属性

border-box（将内容区域压缩）

CSS媒体查询
必须先设置以下内容，媒体查询才有效
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<style media="screen">
	body {
       background-color: grey;
	}
	@media only screen and (max-width: 600px) {
       body {
          background-color: green;
	   }
	}
</style>




























































































































