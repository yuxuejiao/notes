传统布局方式：display + position + float   
Flex布局：弹性布局。所有浏览器都支持。
所有容器都可以指定为flex布局。 
块级元素：display: flex
行内元素：display: inline-flex  
设定为flex布局后，子元素的float、clear、vertical-align属性将失效。   
指定为flex布局 --- flex容器（默认有两根轴，水平的主轴和垂直的交叉轴。项目默认沿主轴排列。）   
容器内的子元素 --- flex项目   
flex容器的属性：   
- 1、flex-direction   
决定主轴的方向，即决定项目排列方向   
取值：   
    - 1、row：默认值，主轴为水平方向，起点在左端
    - 2、row-reverse：主轴为水平方向，起点在右端
    - 3、column：主轴为垂直方向，起点在上沿
    - 4、column-reverse：主轴为垂直方向，起点在下沿
- 2、flex-wrap   
定义如果项目在轴线上排列不下，如何换行。   
取值：
    - 1、nowrap： 默认值，不换行
    - 2、wrap: 换行，第一行在上方
    - 3、wrap-reverse：换行，第一行在下方
- 3、flex-flow
flex-direction 和 flex-wrap的组合简写方式   
形式：flex-flow: flex-direction flex-wrap   
- 4、justify-content   
定义了项目在**主轴**上的对齐方式   
取值：与主轴方向有关。默认主轴方向为从左到右
    - 1、flex-start：默认值，左对齐
    - 2、flex-end：右对齐
    - 3、center: 居中
    - 4、space-between：两端对齐，项目之间的间隔相等
    - 5、space-around：每个项目两侧的间隔相等，所以项目之间的间隔比项目与边框的间隔大一倍。
- 5、align-items   
定义了项目在**交叉轴**上的对齐方式   
取值：与交叉轴方向有关。默认交叉轴方向从上到下   
    - 1、flex-start：交叉轴的起点对齐
    - 2、flex-end: 交叉轴的终点对齐
    - 3、center: 交叉轴的中点对齐
    - 4、baseline: 项目的第一行文字的基线对齐
    - 5、stretch(默认值)：如果项目未设置高度或者设置为auto，将占满整个容器的高度
- 6、align-content   
定义多根轴线的对齐方式，取值与align-items一致   
flex项目的属性：
- 1、flex-grow: 定义项目的放大比例
取值： 默认值为0。即如果存在剩余空间，也不放大。   
当所有项目的flex-grow属性值都为1，则它们将等分剩余空间。如果一个项目的flex-grow属性值为2，其他为1，则前者占据的剩余空间比其他项多一倍。
- 2、flex-shrink：定义项目的缩小比例。默认为1，即如果空间不足，该空间将缩小。   
如果所有项目的flex-shrink属性的值都为1，当空间不足时，它们将等比例缩小。如果一个项目的flex-shrink属性的值为0，其他项目为1，则空间不足时，前者不缩小。
- 3、flex-basis: 定义了在分配多余空间之前，项目占据的主轴空间。默认值为auto，即项目的本来大小。   
它可以设为某个固定的值px，则项目占据固定空间。   
- 4、flex：flex-grow, flex-shrink, flex-basis的简写。默认值为 0 1 auto。   
有两个快捷值： auto(1 1 auto)、none(0 0 auto)
- 5、align-self：允许单个项目有与其他项目不一样的对齐方式，可覆盖父元素的align-items属性。   
默认值为auto，表示继承父元素的属性。   
align-self: auto | flex-start | flex-end | center | baseline | stretch;

