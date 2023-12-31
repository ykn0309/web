## CSS属性书写顺序

建议遵循以下顺序：

* 布局定位属性：display/position/float/clear/visibility/overflow
* 自身属性：width/height/margin/padding/border/background
* 文本属性：color/font/text-decoration/text-align/vertical-align/white-space/break-word
* 其他属性：content/cursor/border-radius/box-shadow/text-shadow/backgrond:linear-gradient...

## CSS定位

### 为什么需要定位

以下情况使用标准流或者浮动无法实现：

* 某个元素可以在一个盒子内移动位置，并且压住其他盒子
* 当我们滚动窗口的时候盒子是固定屏幕某个位置的

### 定位组成

定位是将盒子定在某个位置，按照定位的方式移动盒子

定位=定位模式+边偏移

#### 定位模式

* static 静态定位
* relative 相对定位
* absolute 绝对定位
* fixed 固定定位

它通过CSS的position属性来设置

#### 边偏移

边偏移就是定位的盒子移动到最终位置。有top bottom left right 4个属性

### 静态定位static

静态定位是元素的默认定位方式，无定位的意思

静态定位按照标准流特性摆放位置，它没有边偏移

### 相对定位relative

相对定位是元素在移动位置的时候，是相对于它原来的位置来说的

原来在标准流的位置继续占有，后面的盒子仍然以标准流的方式对待它

### 绝对定位absolute

绝对元素是元素在移动位置的时候，相对于它的祖先元素来说的

* 如果没有父亲或者父元素没有定位，以浏览器为准定位
* 如果祖先元素有定位，则以最近一级有定位的祖先元素为准定位
* 绝对定位不占用原来的位置

### 子绝父相

子级是绝对定位的话，父级就要用相对定位

* 子级绝对定位，不会占有位置，可以放到父盒子的任何一个地方，不会影响其他的兄弟盒子
* 父盒子要加一个定位来限制子盒子在父盒子中
* 父盒子布局时，需要占有位置，所以要用相对定位，如果时绝对定位就不会占有位置

### 固定定位fixed

固定于浏览器可视区的某个位置

* 跟父元素没有任何关系
* 不随滚动条滚动
* 固定定位不占用原来的位置

### 粘性定位sticky

相对定位和固定定位的混合

* 以浏览器的可是窗口为参照点移动元素（固定定位特点）
* 粘性定位占有原先的位置
* 必须添加上下左右的其中一个才有效
