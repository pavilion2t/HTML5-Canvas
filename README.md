# H5 Canvas简介

HTML文本标记语言。
Canvas是屏幕上一个由JS控制的即时模式位图区域。
即时模式☞在画布上呈现像素的方式：Canvas通过JS调用API，在每一帧钟完全重绘屏幕上的位图。
程序员要做的就是在每一帧渲染之前设置屏幕的显示内容，这样就能显示正确的像素。

保留模式：Flash/Silverlight/SVG 对象显示列表由图形渲染器保存，通过在代码中设置属性控制展示在屏幕上的对象。程序员可以远离底层操作，但是它弱化了对位图屏幕最终渲染效果的控制。

基本H5 Canvas API包括一个2D环境，允许绘制各种图形和渲染文本，并将图像直接显示在浏览器窗口定义的区域。（颜色，旋转，渐变色填充，透明度，像素处理/ 使用各种直线，曲线，边框和底纹来增强其效果）

利用modernizer.js来判断各个浏览器支持哪些canvas新特性。

Canvas放入H5页面要做的第一件事情：看页面是否已经加载，所有元素是否都已经展现。
在canvas处理图像和声音的时候，这一点非常重要。（？？？）

所以，这里要使用JS事件。当定义的事件发生时，事件从对象发出，其他对象监听事件，这样就可以基于事件进行处理。JS可以监听对象的一些常见事件（键盘输入，鼠标移动和加载结束等）。

第一个要监听的事件是window对象的load事件，改事件在页面加载结束时发生。
为事件添加监听器，可以使用DOM的对象的addEventListener()方法,接收3个参数：
·load事件
·eventWindowLoaded()事件处理器函数
·useCapture:true/false
  ```
window.addEventListener(“load”,eventWindowLoaded,false);
Function eventWindowLoaded(){
   canvasApp();
}
  ```

也可以用许多其他方式为load事件设置事件监听器：
  ```
  Window.onload = function(){
    canvasApp();
   }
  ```
或者：
```
window.onload = canvasApp;
```




![chapter01](./chapter01/123.gif)
