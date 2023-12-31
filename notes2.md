# HTML

HTML：超文本标记语言

##### 浏览器内核

负责读取网页内容，整理讯息，计算网页的显示方式并显示页面

##### web标准

W3C：万维网联盟

符合web标准，不同浏览器显示相同内容

##### web标准的构成

* 结构：HTML
* 表现：CSS
* 行为：JS

三者中结构最重要

## HTML标签

### 语法规范

HTML标签是由尖括号包围的关键词，通常是成对出现，成为双标签，也有单标签

#### 标签关系

* 包含关系
* 并列关系

### 基本结构标签

* HTML标签：根标签
* head标签：头部
* title标签：标题
* body标签：主体

### 开发工具

#### 文档类型声明标签

```html
<!DOCTYPE html>
```

#### lang语言种类

en英语

zh-CN中文

```html
<html lang="zh_CN">
```

#### 字符集

```html
<meta charset="UTF-8"/>
```

### 常用标签

#### 标签语义

* 标题标签

* HTML提供了六个等级的网页标题

  \<h1>-\<h6>

* 段落和换行标签

  \<p>用于定义段落

  \<br />强制换行标签 break

* 文本格式化标签

  粗体、斜体、下划线

  * 加粗\<strong></ strong>或\<b></ b>
  * 倾斜em或i
  * 删除del或s
  * 下划线ins或u

* div和span标签

  它们就是一个盒子，用来装内容

  division分割

  span跨度

* 图像标签

  src图像路径

  alt替换文本，图像显示不出时显示的文字

  title提示文本，鼠标放在图片上提示的文本

  width设置图像宽度

  height设置图像宽度

  border设置边框宽度

  ```html
     <img src="OIP-C.jpg" alt=""><br />
      <img src="1.ipg" alt="替换文本，图片不能显示">
  ```

* 路径

  目录文件夹

  根目录：打开目录文件夹的第一层

  * 相对路径

    图片相对于HTML页面的路径

    * 同一级路径：直接写文件名
    * 下一级路径：/
    * 上一级路径：../

  * 绝对路径

* 超链接标签

  \<a href="跳转目标" target="弹出方式">文本或图像\</a> anchor

  _self当前页面弹出

  _blank新标签页打开

  连接分类：

  * 外部链接 

  * 内部链接

    网站内部页面之间的相互连接

  * 空链接href=#

  * 下载链接:如果地址里是一个文件，直接下载

  * 网页元素链接

    文本，图像，视频，音频都可以添加超链接

  * 锚点链接

    点击链接，快速定位到页面中的某个位置

    href=#name

### 注释和特殊字符

<!--xxx--> 

* &nbsp: one space

* &lt: less than

* &gt: greater than

  ![image-20230717094300567](C:\Users\杨凯楠\AppData\Roaming\Typora\typora-user-images\image-20230717094300567.png)

### 表格标签

<table>
    <tr>
        <td>姓名</td>
        <td>性别</td>
        <td>年龄</td>
    </tr>
</table>


#### 表头单元格标签

th

#### 表格属性

后期通过css来设置

* align: left center right
* border: 1或""
* cellpadding:像素值 默认为1 文字距离单元格边框的距离
* cellspacing:单元格和单元格之间的距离，默认为1
* width:表格的宽度
* height

#### 表格结构标签

thead  tbody

#### 合并单元格

* 跨行合并
* 跨列合并

### 列表标签

* 无序列表

  ul

  li

  ul中只能放li标签，但是li中可以放任何标签

* 有序列表

  ol

* 自定义列表

  dl定义列表

  dt

  dd

### 表单标签

收集用户信息

* 表单域

  form：action method name

* 表单控件

  * input输入表单元素

    type属性值

    * text
    * password密码
    * radio单选按钮
    * checkbox复选框
    * submit提交
    * reset重置
    * button
    * file：上传文件

    name：性别单选按钮必须有相同的    name才会多选一

    value：规定input元素的值

    checked：当页面打开的时候默认选中

    maxlength：输入最大字符长度

  * select下拉表单元素

    有多个选项让用户选择，并且想要节约页面控件

    select option

    selected="selected"默认选中

  * textarea文本域元素

    用户输入内容比较多时使用

* 提示信息

#### label标签 

label标签的for属性应当与相关元素的id属性相同

# css

## 选择器

### 基础选择器

#### 标签选择器

HTML标签名作为选择器

#### 类选择器

单独选择其中的一个或几个标签

.类名{

​	属性：xxx;

}

多类名，一个标签指定多个类名

#### id选择器

以id属性来设置id选择器

样式#定义，结构id调用，只能调用一次

#### 通配符选择器

表示选取页面中所有元素（标签）

通配选择器不需要调用，自动就给所有元素使用样式

#### 字体属性

标题标签比较特殊，需要单独指定文字大小

##### 字体复合属性

font: style weight size/行高 family（顺序）

不想要的属性可以不写，但是size和family必须要写

#### css文本属性

##### 文本颜色

三种表示方式 

* 预定义的颜色值：red
* 十六进制：#FF0000
* RGB代码：rgb(255,0,0)

##### 对齐文本

text-align用于设置元素内文本内容的水平对齐方式，有三种属性center right left(default)

##### 装饰文本 

text-decoration:

* none(default)：可以去除超链接的下划线
* underline
* overline
* line-through删除线

##### 文本缩进

text-indent:10px (-10px向左缩进) 2em(相对于当前文字大小)

##### 行间距

line-height: 26px

行间距包含上下间距和文本高度

### CSS引入方式

* 内部样式表：写在html页面内部

  通过这种方式可以控制整个页面的元素样式设置，成为嵌入式引入

* 行内样式表

  <p style="color: red; font-size: 20px;">行内样式</p>

  可以控制当前标签设置样式，称为行内式引入

* 外部样式表

  适合于样式比较多的情况，样式单独写到css文件中。在html文件中，用<link>标签引入

### Emmett语法

生成多个标签div*3

包含ul>li

并列div+p

### 复合选择器

#### 后代选择器

又称为包含选择器

ol(元素1) li(元素2) {

}

元素1和元素2可以时任意选择器，包括类名

.nav ul li {

}

#### 子选择器

只能选择亲儿子

元素1>元素2 {

}

#### 并集选择器

div, p {

}

#### 伪类选择器

用于向某些选择器添加特殊的效果

最大的特点是使用 :

a:link 选择所有未访问过的链接

a:visited 访问过的链接

a:hover 鼠标经过的链接

a:active 活动的链接，选择的是鼠标正在按下好没有松开的链接

为了确保伪类选择器能够生效，按照LVHA的顺序声明

##### focus伪类选择器

用于选取获得焦点的表单元素

## CSS元素显示模式

元素以什么方式进行显示

HTML元素一般分为块元素和行内元素两种类型

### 块元素

常见的块元素有h1-h6 p div ul ol li

特点是

* 独占一行
* 高度宽度外边距及内边距都可以控制
* 宽度默认是容器（父级宽度）的100%
* 是一个容器及盒子，里面可以放行内或者块级元素

> 文字类元素内不能放块元素

### 行内元素

常见的行内元素有a strong b em i del span s ins u  

特点是

* 相邻行内元素在一行上，一行可以显示多个
* 高，宽直接设置是无效的
* 默认宽度就是他本身内容的宽度
* 行内元素只能容纳文本或者其他行内元素

> 链接里面不能再放链接
>
> 特殊情况<a>中可以放块级元素，但是a转换一下块级模式最安全

### 行内块元素

img/  input/  td

同时具有块元素和行内元素的特点

* 和相邻行内元素（行内块）在一行上，但是它们之间会有空白间隙。一行可以显示多个（行内元素特点）
* 默认宽度就是他本身内容的宽度（行内元素特点）
* 高度行高外边距以及内边距都可以控制（块级元素特点）

### 元素显示模式转换

特殊情况下，我们需要元素模式的转换，比如想要增加链接<a>的触发范围

display:block;

display:inline;

display:inline-block

## CSS的背景

### 背景颜色

背景颜色的默认值为transparent

### 背景图片

background-img

### 背景平铺

background-repeat: no-repeat不平铺

repeat-x

repeat-y

默认平铺repeat

### 背景图片位置

background-position: x y;

可以使用方位名词或精确单位

参数是方位名词，如果有两个参数，顺序无关

如果是精确位置，第一个一定是x坐标，第二个一定是y坐标

如果只指定一个数值，则一定是x，y默认垂直居中

精确单位可以和方位名词混用

### 背景图像固定

background-attachment属性设置背景图像是否固定或者随着页面的其余部分滚动，后期可以制作视差滚动的效果

取值： fixed（背景图像固定） scroll（背景图像是随着对象内容滚动）

### 背景的复合写法

background:背景颜色 背景图片 背景平铺 背景图片滚动 背景图片位置

这是实际开发中提倡的写法

### 背景色半透明

background:rgba(0,0,0,0.3)

 盒子里面的内容不受影响

## CSS三大特性

### 层叠性

主要解决样式冲突

存在样式冲突时，遵循就近原则，哪个样式离结构距离近就执行哪个样式

样式不冲突就不会层叠

### 继承性

子标签会继承父标签中的样式

恰当地使用可以简化代码，降低css样式的复杂性

#### 行高的继承

行高可以跟单位也可以不跟单位，代表当前元素文字大小的倍数

### 优先级

当一个元素指定多个选择器，就会有优先级的产生

* 选择器相同，则执行层叠性

* 选择器不同，则根据选择器权重执行

* 

  | 选择器               | 选择器权重 |
  | -------------------- | ---------- |
  | 继承或者*            | 0,0,0,0    |
  | 元素选择器           | 0,0,0,1    |
  | 类选择器，伪类选择器 | 0,0,1,0    |
  | ID选择器             | 0,1,0,0    |
  | 行内样式 style=""    | 1,0,0,0    |
  | !important重要的     | ∞          |

  权重叠加：复合选择器会有权重叠加的问题

  ul li:0001+0001=0002

  权重虽然会叠加但是不会进位

## CSS盒子模型

### 盒子模型的组成

边框 外边距 内边距 实际元素

border margin padding content

### 边框border

边框宽度 样式 颜色

border:  border-width || border-style||border-color

solid实线边框

dashed虚线边框

dotted点线边框

可以分别设置上下左右四个边框

### 表格的细线边框

border-collapse 合并相邻的边框

### 内边距padding

可以分别设置上下左右四个内边距

padding-left:20px

padding:

* 一个值代表上下左右边距
* 2个值：上下和左右
* 3个值：上 左右 下
* 4个值：上 右 下 左 顺时针

padding会影响盒子实际大小

如果盒子本身没有指定width/height属性。则此时padding不会撑开盒子大小

### 外边距margin

控制盒子和盒子之间的距离

left right top bottom

简写方式和padding完全一致

### 外边距的典型应用

外边距可以让块级盒子水平居中，但是必须满足两个条件：

* 盒子必须指定了宽度
* 盒子左右的外边距都设置为auto

margin: 0 auto

> 注意：以上方法是让块级元素水平居中，行内元素或者行内块元素水平居中给其父元素添加text-align:center即可

### 外边距合并

使用margin定义块元素的垂直外边距时，可能会出现外边距的合并

#### 嵌套块元素垂直外边距的塌陷

对于两个嵌套关系（父子关系）的块元素，父元素有上外边距同时子元素也有上外边距，此时父元素会塌陷较大的外边距值

![image-20230727151743457](C:\Users\杨凯楠\AppData\Roaming\Typora\typora-user-images\image-20230727151743457.png)

> 解决方案：
>
> * 可以为父元素定义上边框
> * 可以为父元素定义上内边距
> * 可以为父元素添加overflow:hidden

![image-20230727153643878](C:\Users\杨凯楠\AppData\Roaming\Typora\typora-user-images\image-20230727153643878.png)

要避免子元素和父元素的上外边距碰在一起，所以可以通过border和padding将两者隔开

### 清除内外边距

网页元素很多都带有默认的内外边距，可以直接将内外边距改为0

行内元素为了照顾兼容性，尽量只设置左右内外边距，不要设置上下内外边距，但是转换为块级和行内块元素就可以了

### 去掉li前面的圆点

list-style: none;

### 圆角边框

border-radius: 10px

可以通过圆角边框得到圆形的边框

可以用百分比表示盒子长和宽的比例

可以为四个角设置不同的圆角，只需多加几个参数

### 盒子阴影

box-shadow: h-shadow v-shadow blur spread color inset;

| 值       | 描述                           |
| -------- | ------------------------------ |
| h-shadow | 必需，水平阴影的位置，允许负值 |
| v-shadow | 必须，垂直阴影的位置，允许负值 |
| blur     | 可选，模糊距离                 |
| spread   | 可选，阴影的尺寸               |
| color    | 可选，阴影的颜色               |
| inset    | 可选，将外部阴影改为内部阴影   |

盒子阴影不占用空间

可以使用:hover添加鼠标经过时的阴影效果

### 文字阴影

text-shadow:

* h-shadow
* v-shadow
* blur
* color

## CSS浮动

### 传统网页布局的三种方式

* 标准流：标签按照规定好的默认方式排列
* 浮动
* 定位

### 为什么需要浮动

行内块中间会有空隙，不容易控制

一行的左右两端有两个盒子

浮动可以改变默认样式

多个块级元素纵向排列使用标准流，多个块级元素横向排列使用浮动

### 浮动

<p style="color: red;">float</p>属性用于创建浮动框，将其移动到一边，知道左边缘或右边缘触及包含块或者另一个浮动框的边缘

### 浮动特性

* 浮动元素会脱离标准流 **脱标**，浮动的盒子不再保留原先的位置

* **行显示：**如果多个盒子都设置了浮动，则它们会按照属性值在一行内显示并且顶端对齐排列

* **浮动元素具有行内块元素特点：**任何元素都可以浮动。不管原先时什么模式的元素，添加浮动之后具有行内块元素相似的特征

  如果行内元素有了浮动，则不需要转换块级或行内块元素就可以直接给高度和宽度

### 浮动元素经常和标准流父级元素搭配使用

先用标准流的父元素排列上下位置，之后内部子元素采取浮动排列左右位置，符合网页布局第一准则



### 清除浮动方法

* 额外标签法也称隔墙法

  额外标签法会在浮动元素末尾添加一个空的标签（必须是块级元素）。例如\<div style="clear:both">\</div>清除

  * 优点：通俗易懂
  * 缺点：添加了多余的标签

* 父级添加overflow属性

  overflow:hidden

  * 优点：代码简洁
  * 缺点：无法显示溢出的部分

* 父级添加after伪元素

  ![image-20230730020001940](C:\Users\杨凯楠\AppData\Roaming\Typora\typora-user-images\image-20230730020001940.png)

  * 优点：没有增加标签，结构更简单
  * 缺点：照顾低版本浏览器

* 父级添加双伪元素

* ![image-20230730020601876](C:\Users\杨凯楠\AppData\Roaming\Typora\typora-user-images\image-20230730020601876.png)

  优缺点同上

## PS切图

### 图层切图

### 切片切图

### PS插件切图