
# css编码

[1 前端css书写规范](#user-content-1)

[2 公共css文件](#user-content-2)

[3 定义变量css文件](#user-content-3)

[4 定义混合方法css文件](#user-content-4)

[5 定义加载图标css文件](#user-content-5)


## <span id="user-content-1">1 前端css书写规范</span>

css在各行各业都有着广泛的应用，html和css代码风格形成了一定的规范，本项目直接就参考阿里的js规范，不依次列举了。
[前端HTML-CSS规范]  <https://yq.aliyun.com/articles/51487>


##<span id="user-content-2">2 公共css文件</span>

##### Main.scss重要存放影响全局样式和常用样式。
示例：
```scss
@import "./Default";
/*全局样式*/
body {
  background: $grey !important;
  font-family: $font-family !important;
}

/*常用样式*/
.clearfix:after {
  display: block;
  clear: both;
  content: "";
  visibility: hidden;
  height: 0
}
.clearfix {
  zoom: 1
}
.lf {
  float: left;
}
.rf {
  float: right;
}
```
##<span id="user-content-3">3 定义变量css文件</span>

##### Default.scss定义常用变量文件。
示例：
```scss
/*font*/
$font-family: PingFangSC-Regular, 微软雅黑;
$font-color: #595757;
$font-size: 14px;
$font-size12: 12pt;
$font-size14: 14pt;

/*a*/
$a-color: $font-color;
$a-color-hover: #3CA1C9;
/*color*/
$blue-1:#ecf6fd;
$blue-2:#ecf6fd;
$blue-3:#d2eafb;
$blue-4:#7ec2f3;
$blue-5:#49a9ee;
``````
##<span id="user-content-4">4 定义混合方法css文件</span>

##### Minxins.scss定义常用方法以及自动完善兼容方法。
示例：
```scss
@mixin border-radius($radius) {
  -webkit-border-radius: $radius; 
  -moz-border-radius: $radius; 
  -khtml-border-radius: $radius; 
  border-radius: $radius;
}
@mixin box-shadow($shadow...){
  -webkit-box-shadow: $shadow;
  -moz-box-shadow: $shadow; 
  -khtml-box-shadow: $shadow;
  box-shadow: $shadow;
}
//宽高
@mixin wh($width, $height){
  width: $width;
  height: $height;
}

``````
##<span id="user-content-5">5 定义加载图标css文件</span>

##### Icomoon.scss定义引用外部icon方法。
示例：
```css
@font-face {
  font-family: 'icomoon';
  src: url('fonts/icomoon.eot?jo2yei');
  src: url('fonts/icomoon.eot?jo2yei#iefix') format('embedded-opentype'),
  url('fonts/icomoon.ttf?jo2yei') format('truetype'),
  url('fonts/icomoon.woff?jo2yei') format('woff'),
  url('fonts/icomoon.svg?jo2yei#icomoon') format('svg');
  font-weight: normal;
  font-style: normal;
}

[class^="icon-"], [class*=" icon-"] {
  /* use !important to prevent issues with browser extensions that change fonts */
  font-family: 'icomoon' !important;
  speak: none;
  font-style: normal;
  font-weight: normal;
  font-variant: normal;
  text-transform: none;
  line-height: 1;

  /* Better Font Rendering =========== */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.icon-cooperation:before {
  content: "\e900";
}

.icon-respect:before {
  content: "\e901";
}

.icon-response:before {
  content: "\e902";
}

.icon-sincerity:before {
  content: "\e903";
}

``````