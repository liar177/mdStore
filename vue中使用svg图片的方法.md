vue中使用svg图片的方法

一. 由来：如果直接在vue中直接引入svg文件，会因为vue不能识别而无法使用。svg是xml格式的文本文件，vue项目默认情况下只能识别一些常用的图片格式（例如JPG、PNG等等）。

二. 解决方法：

一般情况下，我们想要在vue项目中使用svg图片，有三种方法可以走：

​	1. 通过工具（iconfont、 svg2vue.com 等）将svg转成PNG等vue能识别的格式 ；

	2. webpack中加入相关插件（例如svg-sprite-loader）；
 	3. 利用主流浏览器都能打开svg图片的特性，新建一Vue component，在组件中的template标签中放入svg图片源码，并在需要用的地方引入这个svg组件注册、使用即可；如下图所示

![1698046263052](E:\study\svg in vue\svg1.png)

![1698115294697](E:\study\svg in vue\svg2.png)

但是一般情况下我们获取到的svg文件中，除了svg标签之外还会带着这两个标签：

```xml
<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
```

怎么整合到vue component里面呢？

![1698115585053](E:\study\svg in vue\svg3.png)