# Android-line-height
Android浏览器下line-height垂直居中偏离问题


在Android浏览器下，当字体小于12px或使用em/rem，换算后小于12px时，字体都会强制以12px显示，就导致了这个问题

解决方法一

小于12px的字体统一设置为12px

解决方法二

字体设置为2倍，在缩放0.5倍
```css
.label {
  height: 40px;
  line-height: 40px;
  font-size: 20px;
  border: 1px solid #000;
  -webkit-transform: scale(0.5);
  transform: scale(0.5);
  -webkit-transform-origin: 100% 100%;
  transform-origin: 100% 100%;
}
```

解决方法三

display：table;
```html
<!DOCTYPE html>
<html>
<head>
<title>sss</title>
<style type="text/css">
.btn{
  border: 1px solid #aaa;
  height: 50px;
  width: 100px;
  display: table;
}
</style>
 </head>
<body>
 
<div class="btn">
  <p>我居中了</p>
</div>
</body>
</html>

```
<a href="https://www.zhihu.com/question/39516424">参考链接</a>
