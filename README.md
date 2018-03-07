# myWork

- [移动端配适](#移动端配适)
- [初始化样式](#初始化样式)

## 移动端配适

> 放在公共common.js中

```js
// 自执行
(function(){
  function w() {
    var r = document.documentElement; //根元素html
    var a = r.getBoundingClientRect().width;
    if (a > 750 ){
      a = 750;
    }
    rem = a / 7.5;
    r.style.fontSize = rem + "px";
  }
  w();
  var t;
  window.addEventListener("resize", function() {
    clearTimeout(t);
    t = setTimeout(w, 1000/60);
  }, false);
})();
```

> 然后在重置common.css中设置

```css
/*重置样式*/
html{font-size:calc(100vw/7.5)}
```

[↑ 返回Top](#mywork)

## 初始化样式

### 移动端

```css
/*重置样式*/
html {font-size:calc(100vw/7.5)}
/* body{touch-action:none} */
body,div,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,input,textarea,p,blockquote {
  padding: 0;
  margin: 0;
  font: inherit;
  box-sizing:border-box;
}
input {
  /*在移动端清除浏览器默认样式*/
  -webkit-appearance: none;
  border: none;
}
img {
  border:0;
  vertical-align: top;
}
address,caption,cite,code,dfn,em,strong,th,var,i {
  font-weight: normal;
  font-style: normal;
}
ol,ul,li {
  list-style: none;
}
caption,th {
  text-align: left;
}
h1,h2,h3,h4,h5,h6 {
  font-weight: normal;
  font-size: 100%;
}
q:before,q:after {
  content:'';
}
abbr,acronym { 
  border: 0;
}

/*通用样式*/
body {
  width:7.5rem;
  margin:0 auto;
  font-family: "Helvetica Neue", Helvetica, STHeiTi, sans-serif , "Microsoft YaHei",arial;
  background-color: #f6f6f6;
  color: #626454;
  font-size:.28rem;
  letter-spacing:.03rem;
}
a:link,a:visited {
  text-decoration: none;
  color:#666;
}
a{
  border:none;
  -webkit-tap-highlight-color: rgba(0,0,0,0);
  -webkit-tap-highlight-color:transparent;
  outline:none；
}
input[type=button], input[type=submit], input[type=file], button { cursor: pointer; -webkit-appearance: none; }
:focus{
    outline:0;
}
a,input,textarea{-webkit-tap-highlight-color:rgba(255,0,0,0);}
.fl {
  float:left;
}
.fr {
  float: right;
}
.clearfix:after {
  content: ".";
  visibility: hidden;
  display: block;
  font-size: 0;
  clear: both;
  height: 0;
  line-height: 0;
}
.clearfix {
  *zoom:1;
}
.in-block{
  display:inline-block;
}
.por {
  position: relative;
}
.poa {
  position: absolute;
}
.tran {
  transition:all .3s;
}
.dfr{
  display: flex;
  flex-direction: row;
}
.dfc{
  display: flex;
  flex-direction: column;
}

/*字号*/
.fb{
  font-weight: bold;
}
.fz18{
  font-size: 0.18rem
}
.fz20{
  font-size: 0.2rem;
}

/*字体颜色*/
.fcf{
  color: #fff;
}
.fcfe36{
  color: #fe366a;
}
.fc999{
  color: #999999;
}
.fc666{
  color: #666666;
}
.fc333{
  color: #333333;
}

/*通用边框*/
.bE6{
  border: .01rem solid #E6E6E6;
}
```

### PC端

```css
html, body, div, h1, h2, h3, h4, h5, h6, p, dl, dt, dd, ol, ul, li, fieldset, form, label, input, legend, table, caption, tbody, tfoot, thead, tr, th, td, textarea, article, aside, audio, canvas, figure, footer, header, mark, menu, nav, section, time, video  { margin: 0; padding: 0; box-sizing: border-box; }
 *, *:before, *:after {
  box-sizing: inherit;
}
h1, h2, h3, h4, h5, h6 { font-size: 100%; font-weight: normal }
article, aside, dialog, figure, footer, header, hgroup, nav, section, blockquote { display: block; }
ul, ol { list-style: none; }
img { border: 0 none; vertical-align: top; }
blockquote, q { quotes: none; }
blockquote:before, blockquote:after, q:before, q:after { content: none; }
table { border-collapse: collapse; border-spacing: 0; }
strong, em, i { font-style: normal; font-weight: normal; }
ins { text-decoration: underline; }
del { text-decoration: line-through; }
mark { background: none; }
input::-ms-clear { display: none !important; }
body { font: 12px/1.5 \5FAE\8F6F\96C5\9ED1, \5B8B\4F53, "Hiragino Sans GB", STHeiti, "WenQuanYi Micro Hei", "Droid Sans Fallback", SimSun, sans-serif; background: #fff; }
a { text-decoration: none; color: #333; }
a:hover { text-decoration: underline; }
```

[↑ 返回Top](#mywork)

## sd