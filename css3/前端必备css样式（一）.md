<!--
 * @Description: 
 * @Author: Chuang Li
 * @Date: 2021-09-10 10:50:07
 * @LastEditTime: 2021-09-10 10:50:19
 * @LastEditors: Chuang Li
-->
# 前端必备css样式（一）

## 是什么

收集 整理一些代码块，强化记忆



## 文字截断

```
// 单行
.ellipsis{width:200px;overflow: hidden;white-space: nowrap;text-overflow: ellipsis;}

// 多行
.ellipsis{
    width:200px;
    word-break: break-all;
    text-overflow: ellipsis;
    display: -webkit-box; //对象作为伸缩盒子模型显示
    -webkit-box-orient: vertical; //设置或检索伸缩盒对象的子元素的排列方式
    -webkit-line-clamp: 3; //显示的行数
    overflow: hidden;  // 隐藏超出的内容
}

```

### flex居中

```
.error-page{
  display: flex
  align-items: center
  justify-content: center
  text-align: center
  height: 100%
  font-family: Arial, "Helvetica Neue", Helvetica, sans-serif
}
```

### 横向滚动条不换行

```
.classData .list_date{clear:both;overflow:hidden;width:90%;height:50px;margin:0px auto;overflow-x:scroll;white-space:nowrap;}
.classData .list_date a{display:inline-block;width:40px;height:40px;line-height:40px;margin-left:3px;margin-bottom:10px;text-align:center;border-radius:50%;background-color:#fbfbfb;border:1px solid #eaeaea;color:#777777;}
```
### 鼠标样式

```
cursor:pointer;move;help;
```
### div使用

```
1. div使用规范，最好少嵌套div
2. 行内元素 span a b  strong u i  
3. 块级元素： div h1 p 独有margin padding 
4. 如果想同行需要float才能上来。 
5. div的作用是用来划分区块，不要把div应用到具体的元素上比如文本，图片等，主要是用来布局
6. visibility隐藏元素，隐藏内容保留空间位置。
```

### 文字换行
```
div{word-break:break-all;word-wrap:break-word;}
div{word-wrap: break-word;word-break: normal;} 
div{white-space:nowrap;}
```

### 银色按钮

```
a{width: 80px;margin: 10px 16px 0 0;height: 32px;line-height: 16px;padding: 6px 10px;border: 1px solid #D1D1D1;text-align: center;background: whiteSmoke;border-radius: 6px;-moz-border-radius:6px;-webkit-border-radius: 6px;-moz-box-shadow: 0 0 5px #ddd;
-webkit-box-shadow: 0 0 5px #ddd;box-shadow: 0 0 5px #ddd;}
```
### 手机适配

```
<meta id="viewport" name="viewport" content="width=device-width,initial-scale=1.0,minimum-scale=1.0,maximum-scale=1.0">
```

### URL编码

```
1. 传递参数时需要使用encodeURIComponent

2. 进行url跳转时可以整体使用encodeURI

3. js使用数据时可以使用escape
```

### 空行


```
.vspace{height:8px; font-size:0; line-height:0; width:100%; clear:both;}
```
### 网页文字选择背景色


```
::selection{background: #A8141B; color: white;}
::-moz-selection{background: #A8141B; color:white;}
```


### 固定定位


```
.header{position:fixed; top:0; left:0; width:100%; height:32px; line-height:32px; _position:absolute;}
```
### 透明度


```
.opacity{background:#000;filter:alpha(opacity=30);opacity:0.3;-moz-opacity:0.3;-khtml-opacity: 0.3; background:rgba(0,0,0,.3);}
```

### 圆角

```
-moz-border-radius:4px;
-moz-border-radius-topleft:4px;
-moz-border-radius-topright:4px;
-moz-border-radius-bottomleft:4px;
-moz-border-radius-bottomright:4px;
```
### 边框阴影 box-shadow

```
box-shadow: 3px 3px 30px rgba(0,0,0,.5),
-3px -3px 30px rgba(0,0,0,.5);
```

### 文字阴影  text-shadow

```
text-shadow: 2px 2px 2px #000;
```

### 图片居中


```
.Image{display:inline;text-align:center;} // 或
.Image{display:table-cell;vertical-align:middle;}
```
###  块级元素 行内元素


```
块级元素 <div>，<p>，<h1>，<form>，<ul>  <li>

行内元素 <span>，<a>，<label>，<input>，<img>，<strong>  <em>
```

### h5 属性

```
contenteditable
```

### 文字模糊处理

```
p {color:transparent; text-shadow: #111 0 0 5px;}
```

### hack

```
_  ie6内核识别 _color:#f90  
*  ie7及以下内核识别 *color:#f90  
\9 ie9以下内核识别 color:#f90\9
!important多内核识别 color:#333 !important
```

### 单双数隔行变色

```
// 单数
.wx_table tr:nth-child(odd){background:#f8f8f8;}
// 双数
.wx_table tr:nth-child(even){background:#f8f8f8;}
```
### 360度 旋转

```
.iaudio .imgAudio{float:left;width:25%;height:60px;position:relative;}
.iaudio .imgAudio img{position:absolute;width:60px;height:60px;left:0;top:0;-webkit-animation:loadRotate 3s linear infinite;
  -webkit-animation-fill-mode:both;}
@-webkit-keyframes loadRotate{
  from{
    -webkit-transform:rotateZ(0deg);
  }
  to{
    -webkit-transform:rotateZ(360deg);
  }
}
@keyframes loadRotate{
  from{
    transform:rotateZ(0deg);
  }
  to{
    transform:rotateZ(360deg);
  }
}

// 动画开始时事件
o.addEventListener("webkitAnimationStart", function() {
    console.log("动画开始");
})
// 动画重复运动时事件
o.addEventListener("webkitAnimationIteration", function() {
    console.log("动画重复运动");
})
// 动画结束时事件
o.addEventListener("webkitAnimationEnd", function() {
    console.log("动画结束");
})
```
### 表格布局

```
<table class="wx_table">
    <thead>
    	<th>序号</th>
    	<th>文章名称</th>
    	<th>打卡</th>
    	<th>心得</th>
    </thead>
    <tbody>
    	<tr>
		<td>第1天</td>
		<td>学习《教条示龙场诸生》原文及导读</td>
		<td>“两不”</td>
		<td>写心得</td>
    	</tr>
    </tbody>
</table>
```

```
table.wx_table{width:100%;font-size:14px;}
table.wx_table td,table.wx_table th{text-align:center;line-height:40px;}
table.wx_table th{background:#ececec;font-size:14px;color:#747474;font-weight:normal;}
table.wx_table td{font-size: 14px;color:#747474;}
```

### 360浏览器

```
// 若页面需默认用极速核，增加标签
<meta name="renderer" content="webkit"> 
// 若页面需默认用ie兼容内核，增加标签
<meta name="renderer" content="ie-comp">
// 若页面需默认用ie标准内核，增加标签
<meta name="renderer" content="ie-stand">
```

### 从右向左的文字 维语

```
direction:rtl;unicode-bidi:bidi-override;
```
### 滚动条


```
/*css主要部分的样式*//*定义滚动条宽高及背景，宽高分别对应横竖滚动条的尺寸*/
::-webkit-scrollbar {
    width: 10px; /*对垂直流动条有效*/
    height: 10px; /*对水平流动条有效*/
}

/*定义滚动条的轨道颜色、内阴影及圆角*/
::-webkit-scrollbar-track{
    -webkit-box-shadow: inset 0 0 6px rgba(0,0,0,.3);
    background-color: rosybrown;
    border-radius: 3px;
}

/*定义滑块颜色、内阴影及圆角*/
::-webkit-scrollbar-thumb{ 
    border-radius: 7px;
    -webkit-box-shadow: inset 0 0 6px rgba(0,0,0,.3);
    background-color: #E8E8E8;
}

/*定义两端按钮的样式*/
::-webkit-scrollbar-button {
    background-color:cyan;
}

/*定义右下角汇合处的样式*/
::-webkit-scrollbar-corner {
    background:khaki;
}
```
### 伪类

```
a[href$="html"]::before{content:url(images/web.jpg)} 
// <p><a href="index.html">在线web浏览</a></p>
// 伪元素
p::first-line{color:red;}
p::first-letter{color:green;font-size:25px;}
a::before{content:url(qvod.jpg);}
a::after{content:url(qvod.jpg);}
span::selection{background:#F0F;}
```
### placeholder

```
input::-webkit-input-placeholder, textarea::-webkit-input-placeholder {color: #636363;}
input:-moz-placeholder, textarea:-moz-placeholder { color: #636363;}
```

### h5移动端meta

```
<meta charset="UTF-8">
<title></title>
<meta name="description" content="" />
<meta name="keywords" content="" />
<meta name="viewport" content="width=device-width,initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no" />
<meta name="apple-mobile-web-app-title" content="" />
<meta name="apple-mobile-web-app-capable" content="yes" />
<meta name="msapplication-tap-highlight" content="no">
<meta name="apple-mobile-web-app-status-bar-style" content="black" />
<meta name="format-detection" content="telephone=no">
<meta content="telephone=no" name="format-detection" />
<link rel="apple-touch-startup-image" href="" />
<link rel="apple-touch-icon-precomposed" href="" />
<link rel="stylesheet" type="text/css" href="css/thisStyle.css" />
```

###  自适应网页/响应式网页/自适应图片

```
1. 自适应网页 不定宽 给个最大宽度 
2. 响应式网页 定宽 媒介查询
3. 按640 尺寸切好后 缩放 50% 是实际尺寸后作为背景图片 background-size:100% 100% 保持高保真
4. 按640 尺寸切好后 不缩放 用img标签来自动适应图片宽高  img{isplay:block;max-width:100%;} 高度会自适应
5. 如果背景图片内放置内容 内容部分不要用浮动 用原始的宽度百分比来进行文字布局处理 margin:0 auto使文字居中
6. 自适应布局 页面元素 宽度用百分比 文字用em 不设置高度 但是可以给最小高度，最小高度可以是真实图片的像素(或者像素/2)
7. 如果需要浮动 用百分比 设置布局宽度，适度调整margin值 如果浮动后的图片可以 直接控制img标签的宽高 百分比或em 均可
8. http://www.daqianduan.com/6281.html
```

### @font-face

```
@font-face{font-family:'ds'; src:url('diaosi.ttf');}
body{font-family:'ds';font-size:40px}
```

### 背景平铺

```
1. background-size设置参数
2. stretch:把图片的宽高强行设置为容器的宽高
3. contain:让图片适应容器 把它装进容器中同时会留下空白 上下留白
4. cover:让图片遮住容器 不会留下空白

.div{background: url(img/bg_app.jpg) no-repeat center top;width:100%;min-height:640px;margin:0;padding:0;background-size:100% 100%;}
body {
    /* 加载背景图 */
    background-image: url(images/bg.jpg);
    /* 背景图垂直、水平均居中 */
    background-position: center center;
    /* 背景图不平铺 */
    background-repeat: no-repeat;
    /* 当内容高度大于图片高度时，背景图像的位置相对于viewport固定 */
    background-attachment: fixed;
    /* 让背景图基于容器大小伸缩 */
    background-size: cover;
    /* 设置背景颜色，背景图加载过程中会显示背景色 */
    background-color: #7cd8e3;
}

```
### 自适应html/禁止文本缩放/移动端清除输入框内阴影

```
//设计稿宽为640px时，font-size为50px；当改变屏幕宽时，布局会自适应，无论宽高都会等比例响应。
html{font-size:calc(100vw * 50 / 640);}
html {-webkit-text-size-adjust: 100%;}
input,textarea{border: 0; -webkit-appearance: none;}
```
### iphone 手机按钮背景白色


```
input[type="button"], input[type="submit"], input[type="file"], button { cursor: pointer; -webkit-appearance: none;}
```
### 隐藏默认视频播放器


```
video::-webkit-media-controls {display:none !important;}
```
### REM属性
REM属性指的是相对于根元素设置某个元素的字体大小。它同时也可以用作为设置高度等一系列可以用px来标注的单位。

如果你们设计稿标准是iphone5，那么拿到设计稿的时候一定会发现，完全不能按照高保真上的标注来写css，而是将各个值取半

### 背景图片全屏

```
.background{
  display:block;
  position:fixed;
  background-image:url("http://www.conso-mag.com/wp-content/uploads/2014/03/UNE_gravity.jpeg");
  background-size:cover;
  left: -5px; right: -5px; top: -5px; bottom: -5px;
  filter:blur(3px);
  z-index:1;
}
```
### css3 层居中

```
.card{
  display:block;
  position:absolute;
  transform: translateX(-50%) translateY(-50%);
  left:50%;
  top:50%;
  background-color:#fff;
  width:auto;
  height:90vh;
  box-shadow:1px 1px 13px 0 #010006;
  z-index:100;
}
```

### 表单美化

```
/*表单美化*/
.ep_radio{width: 24px;height: 18px;padding-top: 3px;cursor: pointer;text-align: center;margin-right: 10px;background-image: url(img/inputradio.gif);background-repeat: no-repeat;background-position: -24px 5px;margin-left:0;}
.ep_radio .radioclass {opacity: 0;cursor: pointer;-ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=0)";filter: alpha(opacity=0);}
.ep_radio.on{ background-position: 0 5px;}
.ep_checkbox{width: 20px;height: 20px;cursor: pointer;text-align: center;background-image: url(img/inputcheckbox.gif);background-repeat: no-repeat;background-position: 0 0;}
.ep_checkbox .checkboxclass {opacity: 0;cursor: pointer;-ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=0)";filter: alpha(opacity=0);}
.ep_checkbox.on{ background-position: 0 -21px;}
.ep_file{position: relative;display: inline-block;width:80px;height:30px;text-align:center;background: #88c707;border-radius: 4px;overflow: hidden;color: #fff;text-decoration: none;text-indent: 0;line-height: 30px;}
.ep_file input {position: absolute;font-size: 100px;right: 0;top: 0;opacity: 0;}
.ep_file:hover{color:#fff;}
```

### CSS3 属性

```
 // 属性规定动画在播放之前或之后，其动画效果是否可见。
 animation-fill-mode: forwards;
 // 属性定义当元素不面向屏幕时是否可见。
 backface-visibility: visibily;
 // perspective 属性定义 3D 元素距视图的距离，以像素计。该属性允许您改变 3D 元素查看 3D 元素的视图。当为元素定义 perspective 属性时，其子元素会获得透视效果，而不是元素本身。
perspective: 1000px;
transform-style: preserve-3d;

// 过渡效果 属性名称/all/width/color 都可以
transition: all 0.2s

```

### 等分栏

```
:class="(index + 1) % 4==0?'lasted':''"

/班级圈/
.yn18_class_nav{ width:100%; background: #fff; position:relative; left: 0; top:0; z-index:1;}
.yn18_class_nav section{ display:flex; -webkit-box-pack:justify; -webkit-box-align:center; justify-content:space-between; overflow: hidden; height: 1rem; line-height: 1rem; border-bottom: #eee 1px solid;}
.yn18_class_nav section a{ -webkit-box-flex:1; flex:1; text-align:center; font-size: 0.3rem; color: #c5c5c5;}
.yn18_class_nav section a.cur{color: #1477fb; position: relative;}
.yn18_class_nav section a.cur:after{ content: ''; width: 20%; height: .06rem; border-radius: .06rem; background: #1477fb; position: absolute; bottom: 0; left: 40%;}

```

### css3 不包含最后一个

```css
.nav li:not(:last-child) {    
    border-right: 1px solid #666;  
}
```

### 使用CSS重置（reset）

```
*{
    box-sizing:border-box;
    margin:0;
    padding:0
}
```

### body上加入line-height样式

```
body {
    line-height: 1.5;
}
```

### 垂直居中任何元素 (vertical-center anything)

```
html, body {
    height: 100%;    
    margin: 0;  
}    
body {    
    -webkit-align-items: center;    
    -ms-flex-align: center;    
    align-items: center;    
    display: -webkit-flex;    
    display: flex;  
}
```

### 等宽表格单元格

```text
.calendar {    
    table-layout: fixed;  
}
```

### 强制使用属性选择器显示空链接

```
a[href^="http"]:empty::before {    
    content: attr(href);  
}
```

### 使用rem进行全局大小调整；使用em进行局部大小调整

```
在设置根目录的基本字体大小后，例如html字体大小：15px；，可以将包含元素的字体大小设置为rem:

article {    
    font-size: 1.25rem;  
}    
aside {    
    font-size: .9rem;  
}
然后将文本元素的字体大小设置为em

h2 {    
    font-size: 2em;  
}    
p {    
    font-size: 1em;  
}
```

### 隐藏未静音的自动播放视频

```
video[autoplay]:not([muted]) {    
    display: none;  
}
```

