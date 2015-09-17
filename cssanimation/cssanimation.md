#开发“谁去拿外卖”是怎样的体验
##思考
###`CANVAS`or`CSS`? 如何考量的
- 开发速度
- 适配

##开发
###`HTML`相关
1.  `viewprot`
###`CSS`相关
1.  代码规范
2.  基本上直接`class`选择器
3.  `keyframes`我放到最后（和业务有关）
4.  `font-size` & `rem`
5.  多屏适配
6.  优化（列出来，但是放到后面说）
###`JavaScript`相关
1.  封装拓展了些业务中需要的`DOM`操作
2.  `rem`
3.  Safair的坑
4.  原生的`overflow` -> `iScroll`，实现`fixed`效果
5.  空间换时间

##优化
###一些和优化相关的知识
1. 页面渲染过程 (timeline)
2. 重排 & 重绘
3. `layer`?
4. 硬件加速（translate3D, will-change）(demo)
5. 高消耗样式列表 (demo)
6. `requestAnimationFrame` 以及相关的API
7. 读写样式分离 (demo)
8. `Web Animations` (demo)
9. `display` & `visibilty` & `opacity` (demo)
10. `移动端点击`

###我主要做了哪些优化
1. `CSS`属性上的选择
2. 硬件加速
3. 直接用`touchstart`

##适配方案
1. 布局适配
2. 动画适配
3. 字体适配
