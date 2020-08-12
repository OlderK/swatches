# 开发文档
 - 背景颜色采用 hsl(hue[色相],saturation[饱和度],明度[lightness]) 方法
 - 当前屏幕可见区域的大小 [宽:w] = window.innerWidth、[高:h] = window.innerHeight
 - 光标划入时的位置
  + PC端（mousemove） [clientX] = event.pageX 、 [clientY] = event.pageY
  + 移动端 （touchmove）[clientX] = event.touches[0].pageX 、 [clientY] = event.touches[0].pageY
 - 屏幕中心点位置
  + [centerX] = w/2 ; [centerY] = h/2
 - 光标位置与中心点竖直方向的夹角[angle]（0-360）
 - 通过[angle]根据色环（0-360）显示不同色相的原理来获取[色相:hue]
 - 光标位置到中心点的距离[distance]
 - 中心点在[angle]该方向上到边界的最大距离[maxdistance]
 - [lightness] = [distance]/[maxdistance]（0%-100%）设置明度[lightness]
 - 