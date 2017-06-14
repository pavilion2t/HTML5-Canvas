# 2.3 Canvas状态

Canvas环境中绘图，可以利用所谓的绘图堆栈状态。  
每个状态随时存储上下文数据。    
下面是存储在状态堆栈的数据列表：   
  **  变换矩阵信息    
  例如旋转或平移时，使用context.rotate()方法和context.setTransform()方法
 
  **  当前剪贴区域  
  
  **  画布属性的当前值，如下所示：
    globalAlpha    
    globalCompositeOperation  
    strokeStyle   
    textAlign,textBaseline   
    lineCap,lineJoin,lineWidth,and miterLimit   
    fillStyle    
    font   
    shadowBlur,shadowColor,shadowOffsetX,and shadowOffsetY  
    
## 2.3.1 什么不属于状态    
  当前路径和当前位图受Canvas环境控制，不属于保存的状态。

## 2.3.2 如何保存和恢复Canvas状态      

  保存当前状态到堆栈，调用以下函数：  
  调出最后存储到堆栈恢复画布，调用以下函数：   
  
  ```
  context.save()
  context.restore()
  ```
  
#  2.4 使用路径创建线段     

    路径的环境是一个需要理解的重要概念，因为它决定了只能变换画布上的当前路径。
