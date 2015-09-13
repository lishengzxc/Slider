#CSS动画 谁去拿外卖
##演示下
[http://h.ele.me/activities/takefood](http://h.ele.me/activities/takefood)

##分享开发和优化的过程
###开发
####第零个问题 - 选择canvas？
####第一个问题 - 背景循环动画
####第二个问题 - 屏幕的布局适配
####第三个问题 - safari下，改变动画`animation-duration`的问题
####第四个问题 - 为了开发方便，没有用jQuery，拓展了`Element.classList`

###有分享优化过程之前，一些为了优化而需要了解的知识
####页面渲染过程

- Recalculate Style
- Layout
- Paint Setup
- Paint
- Composite Layers

####生成一个Layer

- 拥有3d transform属性
- 使用animation, transition实现opacity, transform的动画
- video
- canvas
- Flash
- 使用CSS filters的元素
- z-index大于某个相邻节点的Layer的元素

####结论：
Layout，Paint，Composite，修改不同CSS属性会触发不同阶段
触发Layout：改变width, height, margin等和大小、位置相关的属性，读取相关属性
触发Paint：当修改(border-radius, box-shadow)高消耗样式, color等展示相关属性时
减少不必的绘制

###重绘属性列表（避免过分重绘）
color border-style visibilty background text-decoration background-image,postion,repeat outline border-radius box-shadow

###关于will-change

Composite：避免意外生成layer

###提一下raf
###提一下Web Animations
[http://web.jobbole.com/82106/](http://web.jobbole.com/82106/)


###优化
####选择那些触发Composite的属性
####滚动的优化
因为在移动端，所以直接选择了iScroll，但是同时也遇到了问题，就是使用iScroll后的fixed问题
####循环上的优化
减少循环，尽可能将需要的状态保存下来（空间换时间）
####display: none？
opacity display: none visibilty
####Click？TouchStart？
移动端的问题



