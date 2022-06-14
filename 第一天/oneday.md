# CSS选择器

## 1.基本选择器

* 通配符选择器
* { margin: 0; padding: 0; border: none; }
* 元素选择*器*

 body { background: #eee; }

* 类选择器

.list { list-style: square; }

* ID选择器

#list { width: 500px; margin: 0 auto; }

* 后代选择器

.list li { margin-top: 10px; background: #abcdef; }

## 2.基本选择器扩展

* 子元素选择器

#wrap > .inner {color: pink;}

也可称为直接后代选择器,此类选择器只能匹配到直接后代，不能匹配到深层次的后代元素

* *相邻兄弟选择器*

 #wrap #first + .inner {color: #f00;}

它只会匹配紧跟着的兄弟元素

* *通用兄弟选择器*

 #wrap #first ~ div { border: 1px solid;}

它会匹配所有的兄弟元素(不需要紧跟)

* *选择器分组*

 h1,h2,h3{color: pink;}

此处的逗号我们称之为结合符

## 3.属性选择器

* *存在和值属性选择器*

[attr]：该选择器选择包含 attr 属性的所有元素，不论 attr 的值为何。

[attr=val]：该选择器仅选择 attr 属性被赋值为 val 的所有元素。

[attr~=val]：表示带有以 attr 命名的属性的元素，并且该属性是一个以空格作为分隔的值列表，其中至少一个值为val。

* *子串值属性选择器*

[attr|=val] : 选择attr属性的值是val（包括val）或以val-开头的元素。

[attr^=val] : 选择attr属性的值以val开头（包括val）的元素。

[attr$=val] : 选择attr属性的值以val结尾（包括val）的元素。

[attr*=val] : 选择attr属性的值中包含字符串val的元素。

* 伪类与伪元素选择器

***链接伪类* **注意:link，:visited，:target是作用于链接元素的！

:link 表示作为超链接，并指向一个未访问的地址的所有锚

:visited 表示作为超链接，并指向一个已访问的地址的所有锚

:target 代表一个特殊的元素，它的id是URI的片段标识符

**动态伪类** 注意:hover，:active基本可以作用于所有的元素！

:hover 表示悬浮到元素上

:active 表示匹配被用户激活的元素（点击按住时）

由于a标签的:link和:visited可以覆盖了所有a标签的状态，所以当:link，:visited，:hover，:active同时出现在a标签

身上时 :link和:visited不能放在最后！！！

***表单相关伪类***

:enabled 匹配可编辑的表单

:disable 匹配被禁用的表单

:checked 匹配被选中的表单

:focus 匹配获焦的表单

***结构性伪类***

index的值从1开始计数！！！！

index可以为变量n(只能是n)

index可以为even odd

#wrap ele:nth-child(index) 表示匹配#wrap中第index的子元素 这个子元素必须是ele

#wrap ele:nth-of-type(index) 表示匹配#wrap中第index的ele子元素

除此之外:nth-child和:nth-of-type有一个很重要的区别！！nth-of-type以元素为中心！！！

:nth-child(index)

表示3的倍数的所有p元素

```css
p:nth-child(3n+0)
```

:first-child

:last-child

:nth-last-child(index)

:only-child

:not

:empty(内容必须是空的，有空格都不行，有attr没关系)

***伪元素***

::after

::before

::selection

# 浏览器默认样式

# 常见元素的类型及特性

# 盒子模型

## 标准盒模型

width 与 height 只包括内容的宽和高， 不包括边框（border），内边距（padding），外边距（margin）。注意: 内边距, 边框 & 外边距 都在这个        盒子的外部。 比如. 如果 .box {width: 350px}; 而且 {border: 10px solid black;} 那么在浏览器中的渲染的实际宽度将是370px;

    尺寸计算公式：

    width = 内容的宽度，

    height = 内容的高度。

    宽度和高度都不包含内容的边框（border）和内边距（padding）。

## 怪异盒模型

  width 和 height 属性包括内容，内边距和边框，但不包括外边距。这是当文档处于 Quirks模式 时Internet Explorer使用的盒模型。

    这里的维度计算为：

    width = border + padding + 内容的  width，

    height = border + padding + 内容的 height

## 实现三角形

## 边框圆角

## 背景

### background-color

### background-image

属性用于为一个元素设置一个或多个背景图像，图像在绘制时，以z轴方向堆叠的方式进行。

注意：background-color会在image之下进行绘制，边框和内容会在image之上进行绘制

### background-repeat

CSS 属性定义背景图像的重复方式。背景图像可以沿着水平轴，垂直轴，两个轴重复，或者根本不重复

### background-position

### background-origin
