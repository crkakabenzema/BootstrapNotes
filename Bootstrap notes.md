# Bootstrap notes

## **一、网格系统**

### 响应式网格系统

系统会自动分为最多12列：数字越大越宽

![image-20201203105636079](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203105636079.png)

|              | 超小设备手机（<768px） | 小型设备平板电脑（≥768px）   | 中型设备台式电脑（≥992px）   | 大型设备台式电脑（≥1200px）  |
| ------------ | ---------------------- | ---------------------------- | ---------------------------- | ---------------------------- |
| 网格行为     | 一直是水平的           | 以折叠开始，断点以上是水平的 | 以折叠开始，断点以上是水平的 | 以折叠开始，断点以上是水平的 |
| 最大容器宽度 | None (auto)            | 750px                        | 970px                        | 1170px                       |
| Class 前缀   | **.col-xs-***          | **.col-sm-***                | **.col-md-***                | **.col-lg-***                |

### 偏移列

使用 **.col-md-offset-\*** 类。这些类会把一个列的左外边距（margin）增加 ***** 列，其中 ***** 范围是从 **1** 到 **11**。

例：

![image-20201203105735037](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203105735037.png)

### 响应式列重叠

可以使用 **.clearfix** class解决

![image-20201203105750223](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203105750223.png)

### 嵌套列

为了在内容中嵌套默认的网格，请添加一个新的 **.row**，并在一个已有的 **.col-md-\*** 列内添加一组 **.col-md-\*** 列，这组列个数不能超过12

![image-20201203105705978](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203105705978.png)   

### 列排序

可以很容易地以一种顺序编写列，然后以另一种顺序显示列。轻易地改变带有 **.col-md-push-\*** 和 **.col-md-pull-\*** 类的内置网格列的顺序，其中 ***** 范围是从 **1** 到 **11**。

## 二、排版类

| lead                | 使段落突出显示                                               |      |
| ------------------- | ------------------------------------------------------------ | ---- |
| .small              | 设定小文本 (设置为父文本的 85% 大小)                         |      |
| .text-left          | 设定文本左对齐                                               |      |
| .text-center        | 设定文本居中对齐                                             |      |
| .text-right         | 设定文本右对齐                                               |      |
| .text-justify       | 设定文本对齐,段落中超出屏幕部分文字自动换行                  |      |
| .text-nowrap        | 段落中超出屏幕部分不换行                                     |      |
| .text-lowercase     | 设定文本小写                                                 |      |
| .text-uppercase     | 设定文本大写                                                 |      |
| .text-capitalize    | 设定单词首字母大写                                           |      |
| .initialism         | 显示在 <abbr> 元素中的文本以小号字体展示，且可以将小写字母转换为大写字母 |      |
| .blockquote-reverse | 设定引用右对齐                                               |      |
| .list-unstyled      | 移除默认的列表样式，列表项中左对齐 ( <ul> 和 <ol> 中)。 这个类仅适用于直接子列表项    (如果需要移除嵌套的列表项，你需要在嵌套的列表中使用该样式) |      |
| .list-inline        | 将所有列表项放置同一行                                       |      |
| .dl-horizontal      | 该类设置了浮动和偏移，应用于 <dl> 元素和 <dt> 元素中，具体实现可以查看实例 |      |
| .pre-scrollable     | 使 <pre> 元素可滚动，代码块区域最大高度为340px,一旦超出这个高度,就会在Y轴出现滚动条 |      |

## 三、表格

下表样式可用于表格中：<table class='table'>

### table类

| 类               | 描述                                            |      |
| ---------------- | ----------------------------------------------- | ---- |
| .table           | 为任意 <table> 添加基本样式 (只有横向分隔线)    |      |
| .table-striped   | 在 <tbody> 内添加斑马线形式的条纹 ( IE8 不支持) |      |
| .table-bordered  | 为所有表格的单元格添加边框                      |      |
| .table-hover     | 在 <tbody> 内的任一行启用鼠标悬停状态           |      |
| .table-condensed | 让表格更加紧凑                                  |      |

### tr, th 和 td 类

下表的类可用于表格的行或者单元格：

| .active  | 将悬停的颜色应用在行或者单元格上 |      |
| -------- | -------------------------------- | ---- |
| .success | 表示成功的操作                   |      |
| .info    | 表示信息变化的操作               |      |
| .warning | 表示一个警告的操作               |      |
| .danger  | 表示一个危险的操作               |      |

### 响应式表格

通过把任意的 *.table* 包在 <div class='table-responsive'>内，您可以让表格水平滚动以适应小型设备

## 四、表单和控件

### 表单：

Bootstrap 提供了下列类型的表单布局：

- 垂直表单（默认）
- 内联表单
- 水平表单

支持最常见的表单控件，主要是 *input、textarea、checkbox、radio 和 select*, 同时向所有的文本元素 <input>、<textarea> 和 <select> 添加 class ="*form-control*"

#### 垂直或基本表单：

- 向父 <form> 元素添加 *role="form"* <form role="form">
- 把标签和控件放在一个带有 class *.form-group* 的 <div> 中。这是获取最佳间距所必需的。

<--! div class='form-group'>

- 向所有的文本元素 <input>、<textarea> 和 <select> 添加 class ="*form-control*" 。

<input type="text" class="form-control" id="name" placeholder="请输入名称">

![image-20201203095541158](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203095541158.png)

#### 内联表单:

如果需要创建一个表单，它的所有元素是内联的，向左对齐的，标签是并排的，请向 <form> 标签添加 class *.form-inline*

![image-20201203095612974](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203095612974.png)

#### 水平表单:

- 向父 <form> 元素添加 class *.form-horizontal*。
- 把标签<label>和控件放在一个带有 class *.form-group* 的 <div> 中。
- 向标签<label>添加 class *.control-label*。

![image-20201203095337930](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203095337930.png)

![image-20201203095429195](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203095429195.png)

### 表单控件

#### 输入框input：

input 类型的支持，包括：*text、password、datetime、datetime-local、date、month、time、week、number、email、url、search、tel* 和 *color*

#### 输入框组input-group:

![image-20201203141901205](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203141901205.png)

##### 输入框组的大小

向 **.input-group** 添加相对表单大小的 class（比如 **.input-group-lg、input-group-sm**）来改变输入框组的大小

![image-20201203142053973](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203142053973.png)

#### 复选框和单选插件

您可以把复选框和单选插件作为输入框组的前缀或者后缀元素

![image-20201203142251675](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203142251675.png)

#### 输入框带按钮插件

![image-20201203142349861](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203142349861.png)

#### 输入框带有下拉菜单

在输入框组中添加带有下拉菜单的按钮，只需要简单地在一个 **.input-group-btn** class  中包裹按钮和下拉菜单即可

![image-20201203142653273](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203142653273.png)

![image-20201203142705085](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203142705085.png)

#### 输入框带有分割的下拉菜单

![image-20201203142854645](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203142854645.png)

![image-20201203142913643](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203142913643.png)

#### 文本框（Textarea):

textarea class="form-control" rows="3" 

可以改变 *rows* 属性（较少的行 = 较小的盒子，较多的行 = 较大的盒子）

#### 复选框（Checkbox）和单选框（Radio):

从列表中选择若干个选项时，请使用 *checkbox*。只能选择一个选项，请使用 *radio*

![image-20201203100702209](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203100702209.png)

![image-20201203100719699](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203100719699.png)

#### 选择框（Select):

- 使用 <select class='form-control'> 展示列表选项，通常是那些用户很熟悉的选择列表，比如州或者数字。
- 使用 <select multiple class='form-control'> 允许用户选择多个选项。

#### 静态控件

当您需要在一个水平表单内的表单标签后放置纯文本时，请在 <p> 上使用 class *.form-control-static*。

#### 表单控件状态

除了 *:focus* 状态（即，用户点击 input 或使用 tab 键聚焦到 input 上），Bootstrap 还为禁用的输入框定义了样式，并提供了表单验证的 class。

##### 输入框焦点

当输入框 input 接收到 *:focus* 时，输入框的轮廓会被移除，同时应用 *box-shadow*。

##### 禁用的输入框 input

如果您想要禁用一个输入框 input，只需要简单地添加 *disabled* 属性，这不仅会禁用输入框，还会改变输入框的样式以及当鼠标的指针悬停在元素上时鼠标指针的样式。

##### 禁用的字段集 fieldset

对 <fieldset> 添加 disabled 属性来禁用 <fieldset> 内的所有控件。

##### 验证状态

Bootstrap 包含了错误、警告和成功消息的验证样式。只需要对父元素简单地添加适当的 class（*.has-warning、 .has-error 或 .has-success*）即可使用验证状态。

![image-20201203101856285](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203101856285.png)

![image-20201203101948943](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203101948943.png)

![image-20201203102012252](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203102012252.png)

#### 表单控件大小

使用 class *.input-lg* 和 *.col-lg-** ，class *.input-sm* 和 *.col-sm-**来设置表单的高度和宽度

![image-20201203102225177](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203102225177.png)

![image-20201203102244286](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203102244286.png)

![image-20201203102306521](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203102306521.png)

#### 表单帮助文本

Bootstrap 表单控件可以在输入框 input 上有一个块级帮助文本。为了添加一个占用整个宽度的内容块，请在 <input> 后使用 *.help-block* 如： <span class="help-block">



## 五、Bootstrap 按钮和按钮组

### 按钮

#### 基本样式

| .btn         | 为按钮添加基本样式                      |      |
| ------------ | --------------------------------------- | ---- |
| .btn-default | 默认/标准按钮                           |      |
| .btn-primary | 原始按钮样式（未被操作）                |      |
| .btn-success | 表示成功的动作                          |      |
| .btn-info    | 该样式可用于要弹出信息的按钮            |      |
| .btn-warning | 表示需要谨慎操作的按钮                  |      |
| .btn-danger  | 表示一个危险动作的按钮操作              |      |
| .btn-link    | 让按钮看起来像个链接 (仍然保留按钮行为) |      |
| .btn-lg      | 制作一个大按钮                          |      |
| .btn-sm      | 制作一个小按钮                          |      |
| .btn-xs      | 制作一个超小按钮                        |      |
| .btn-block   | 块级按钮(拉伸至父元素100%的宽度)        |      |
| .active      | 按钮被点击                              |      |
| .disabled    | 禁用按钮                                |      |

![image-20201203103002686](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203103002686.png)

下表列出了获得各种大小按钮的 class：

| Class      | 描述                                         |
| ---------- | -------------------------------------------- |
| .btn-lg    | 这会让按钮看起来比较大。                     |
| .btn-sm    | 这会让按钮看起来比较小。                     |
| .btn-xs    | 这会让按钮看起来特别小。                     |
| .btn-block | 这会创建块级的按钮，会横跨父元素的全部宽度。 |

#### 关闭图标

使用通用的关闭图标来关闭模态框和警告框

![image-20201203104845625](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203104845625.png)

#### 插入符

使用插入符表示下拉功能和方向

![image-20201203105127860](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203105127860.png)

### 按钮组

在 div 中直接使用 class='btn-group' 可以创建按钮组：

使用 .btn-group-lg|sm|xs 来控制按钮组的大小。如class="btn-group btn-group-lg"

如果要设置垂直方向的按钮可以通过 .btn-group-vertical 类来设置

#### 基本的按钮组

![image-20201203133701554](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203133701554.png)

#### 按钮工具栏

![image-20201203133738774](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203133738774.png)

#### 按钮的大小

![image-20201203133847550](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203133847550.png)

#### 垂直的按钮组

![image-20201203133944476](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203133944476.png)

#### 内嵌下拉菜单的按钮组

按钮组内嵌的按钮可以设置下拉菜单

![image-20201203103826909](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203103826909.png)

![image-20201203103842386](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203103842386.png)

#### 内嵌下拉菜单

使用下拉菜单，只需要在 class **.dropdown** 内加上下拉菜单即可

![image-20201203132932870](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203132932870.png)

![image-20201203132948388](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203132948388.png)

![image-20201203133200195](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203133200195.png)

![image-20201203133223843](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203133223843.png)

#### 分割的按钮下拉菜单

![image-20201203134429486](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203134429486.png)

#### 按钮下拉菜单的大小

**.btn-lg、.btn-sm** 或 **.btn-xs**

![image-20201203134624141](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203134624141.png)

#### 按钮上拉菜单

菜单也可以往上拉伸的，只需要简单地向父 **.btn-group** 容器添加 **.dropup** 即可

![image-20201203134844102](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203134844102.png)



## 六、Bootstrap 图片

### 图片

Bootstrap 提供了三个可对图片应用简单样式的 class：

- *.img-rounded*：添加 *border-radius:6px* 来获得图片圆角。
- *.img-circle*：添加 *border-radius:50%* 来让整个图片变成圆形。
- *.img-thumbnail*：添加一些内边距（padding）和一个灰色的边框。

- *.img-responsive*：图片响应式（将很好地扩展到父元素）。


#### 缩略图

创建缩略图的步骤如下：

- 在图像周围添加带有 class **.thumbnail** 的 <a> 标签。
- 这会添加四个像素的内边距（padding）和一个灰色的边框。
- 当鼠标悬停在图像上时，会动画显示出图像的轮廓。

![image-20201204101810108](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204101810108.png)

![image-20201204101822947](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204101822947.png)

#### 添加自定义内容

可以向缩略图添加各种 HTML 内容，比如标题、段落或按钮

- 把带有  class **.thumbnail** 的 <a> 标签改为 <div>。
- 在该 <div> 内，您可以添加任何您想要添加的东西。由于这是一个 <div>，我们可以使用默认的基于 span 的命名规则来调整大小。
- 如果您想要给多个图像进行分组，请把它们放置在一个无序列表中，且每个列表项向左浮动。

![image-20201204102414065](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204102414065.png)

![image-20201204102430818](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204102430818.png)



## 七、Bootstrap 字体图标(Glyphicons)

![image-20201203131729575](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203131729575.png)

![image-20201203131742619](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203131742619.png)

### 图标列表：

![image-20201203131346208](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203131346208.png)

![image-20201203131359464](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203131359464.png)

![image-20201203131415963](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203131415963.png)

![image-20201203131436514](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203131436514.png)

![image-20201203131455879](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203131455879.png)

![image-20201203131511576](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203131511576.png)

![image-20201203131530651](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203131530651.png)

![image-20201203131544300](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203131544300.png)

![image-20201203131604964](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203131604964.png)

![image-20201203131621167](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203131621167.png)

### 定制字体尺寸

![image-20201203131951625](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203131951625.png)

### 应用文本阴影

![image-20201203132320230](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203132320230.png)

## 八、导航和导航栏

对每个 **.nav** class，如果添加了 **.disabled** class，则会创建一个灰色的链接，同时禁用了该链接的 **:hover** 状态

### 导航

#### 表格导航

![image-20201203144446534](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203144446534.png)

#### 胶囊式导航

![image-20201203144544014](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203144544014.png)

##### 垂直的胶囊式导航

![image-20201203144656662](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203144656662.png)

##### 与父元素等宽的胶囊式导航

![image-20201203144937551](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203144937551.png)

#### 导航带下拉菜单

向标签添加下拉菜单的步骤如下：

- 以一个带有 class **.nav** 的无序列表开始。
- 添加 class **.nav-tabs**。
- 添加带有 **.dropdown-menu** class 的无序列表。

![image-20201203145438195](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203145438195.png)

### 导航栏

导航栏包括了站点名称和基本的导航定义样式

创建一个默认的导航栏的步骤如下：

- 向 <nav> 标签添加 class **.navbar、.navbar-default**。
- 向上面的元素添加 **role="navigation"**，有助于增加可访问性。
- 向 <div> 元素添加一个标题 class **.navbar-header**，内部包含了带有 class **navbar-brand** 的 <a> 元素。这会让文本看起来更大一号。
- 为了向导航栏添加链接，只需要简单地添加带有 class **.nav、.navbar-nav** 的无序列表即可

![image-20201203154320576](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203154320576.png)

#### 响应式的导航栏

折叠的内容必须包裹在带有 class **.collapse、.navbar-collapse** 的 <div> 中。

折叠起来的导航栏实际上是一个带有 class **.navbar-toggle** 及两个 data- 元素的按钮。第一个是 **data-toggle**，用于告诉 JavaScript 需要对按钮做什么，第二个是 **data-target**，指示要切换到哪一个元素。三个带有 class **.icon-bar** 的 <span> 创建所谓的汉堡按钮。这些会切换为 **.nav-collapse** <div> 中的元素

![image-20201203155339391](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203155339391.png)

![image-20201203155354264](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203155354264.png)

#### 导航栏中的表单

使用 **.navbar-form** class

![image-20201203170047226](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203170047226.png)

#### 导航栏中的按钮

使用 class **.navbar-btn** 向不在 <form> 中的 <button> 元素添加按钮，按钮在导航栏上垂直居中

![image-20201203170510377](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203170510377.png)

#### 导航栏中的文本

在导航中包含文本字符串，请使用 class **.navbar-text**。这通常与 <p> 标签一起使用

![image-20201203170702672](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203170702672.png)

#### 导航栏结合图标

使用 class **glyphicon glyphicon-\*** 来设置图标

![image-20201203171536753](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203171536753.png)

#### 导航栏定位

##### 组件对齐方式

使用实用工具 class **.navbar-left** 或 **.navbar-right** 向左或向右对齐导航栏中的 *导航链接、表单、按钮或文本* 这些组件

![image-20201203171946378](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203171946378.png)

![image-20201203172006906](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203172006906.png)

![image-20201203172025404](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203172025404.png)

##### 固定到顶部

导航栏可以动态定位，可以把它放置在页面的顶部或者底部，向 **.navbar class** 添加 class **.navbar-fixed-top**

为了防止导航栏与页面主体中的其他内容的顶部相交错，请向 <body> 标签添加至少 50 像素的内边距

![image-20201203172824991](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203172824991.png)

##### 固定到底部

向 **.navbar class** 添加 class **.navbar-fixed-bottom**

![image-20201203173014405](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203173014405.png)

##### 随页面滚动

向 **.navbar class** 添加 class **.navbar-static-top**

![image-20201203173117585](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203173117585.png)

#### 反色导航栏

向 **.navbar** class 添加 **.navbar-inverse** class 即可

![image-20201203173242435](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203173242435.png)

### 面包屑导航

面包屑导航可以显示发布日期、类别或标签

表示当前页面在导航层次结构内的位置

![image-20201203173710759](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201203173710759.png)

## 九、分页

| .pagination                    | 添加该 class 来在页面上显示分页。                            | `<ul class="pagination">  <li><a href="#">«</a></li>  <li><a href="#">1</a></li>  ....... </ul>` |
| ------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| .disabled, .active             | 您可以自定义链接，通过使用 **.disabled** 来定义不可点击的链接，通过使用 **.active** 来指示当前的页面。 | `<ul class="pagination">  <li class="disabled"><a href="#">«</a></li>  <li class="active"><a href="#">1<span class="sr-only">(current)</span></a></li>  ....... </ul>` |
| .pagination-lg, .pagination-sm | 使用这些 class 来获取不同大小的项。                          | `<ul class="pagination pagination-lg">...</ul> <ul class="pagination">...</ul> <ul class="pagination pagination-sm">...</ul>` |

![image-20201204093512834](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204093512834.png)

## 十、标签和徽章

使用class.label来显示标签

![image-20201204094151614](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204094151614.png)

徽章与标签相似，主要的区别在于徽章的边角更加圆滑

只需要把 **<span class="badge">** 添加到链接、Bootstrap 导航等这些元素上即可

![image-20201204094709891](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204094709891.png)

## 十一、超大屏幕

超大屏幕（Jumbotron）。顾名思义该组件可以增加标题的大小，并为登陆页面内容添加更多的外边距（margin）

创建一个带有 class **.jumbotron**. 的容器 <div>

## 十二、页面标题

在网页标题四周添加适当的间距

![image-20201204100554278](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204100554278.png)

## 十三、警告

警告（Alerts）向用户提供了一种定义消息样式的方式

通过创建一个 <div>，并向其添加一个 **.alert** class 和四个上下文 class（即 **.alert-success、.alert-info、.alert-warning、.alert-danger**）之一，来添加一个基本的警告框

![image-20201204103255724](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204103255724.png)

### 可取消的警告

- 通过创建一个 <div>，并向其添加一个 **.alert** class 和四个上下文 class（即 **.alert-success、.alert-info、.alert-warning、.alert-danger**）之一，来添加一个基本的警告框。
- 同时向上面的 <div> class 添加可选的 **.alert-dismissable**。
- 添加一个关闭按钮。

![image-20201204103632249](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204103632249.png)

### 带连接的警告

- 通过创建一个 <div>，并向其添加一个 **.alert** class 和四个上下文 class（即 **.alert-success、.alert-info、.alert-warning、.alert-danger**）之一，来添加一个基本的警告框。
- 使用 **.alert-link** 实体类来快速提供带有匹配颜色的链接。

![image-20201204103857916](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204103857916.png)

## 十四、进度条

### 默认的进度条

添加一个带有 class **.progress** 的 <div>。

接着，在上面的 <div> 内，添加一个带有 class **.progress-bar** 的空的 <div>。

添加一个带有百分比表示的宽度的 style 属性，例如 style="width: 60%"; 表示进度条在 60% 的位置

![image-20201204105020867](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204105020867.png)

### 交替的进度条

添加一个带有 class **.progress** 的 <div>。

如需条纹，添加一个带有 class **.progress** 和 **.progress-striped** 的 <div>

如需动画，添加一个带有 class **.progress** 、**.progress-striped**和 **active** 的 <div>

如需堆叠，把多个进度条放在相同的 **.progress** 中即可

接着，在上面的 <div> 内，添加一个带有 class **.progress-bar** 和 class **progress-bar-\*** 的空的 <div>。其中，* 可以是 **success、info、warning、danger**。

添加一个带有百分比表示的宽度的 style 属性，例如 style="60%"; 表示进度条在 60% 的位置

![image-20201204105203728](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204105203728.png)

## 十五、多媒体对象

使用 `.media-left` 类让多媒体对象(图片)来实现左对齐，同样 `.media-right` 类实现了右对齐

![image-20201204111332000](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204111332000.png)

### 顶部、底部、居中对齐

![image-20201204111858673](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204111858673.png)

![image-20201204111914231](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204111914231.png)

### 内嵌多媒体对象

![image-20201204112152888](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204112152888.png)

![image-20201204112208094](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204112208094.png)

![image-20201204112228456](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204112228456.png)

## 十六、列表组

### 列表组

- 向元素 <ul> 添加 class **.list-group**。
- 向 <li> 添加 class **.list-group-item**。

![image-20201204113025860](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204113025860.png)

#### 列表组添加勋章

只需要在 <li> 元素中添加 **<span class="badge">** 即可

![image-20201204113134866](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204113134866.png)

#### 列表组水平显示

![image-20201204113339539](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204113339539.png)

## 十七、面板

创建一个基本的面板，只需要向 <div> 元素添加 class **.panel** 和 class **.panel-default** 即可

![image-20201204131917274](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204131917274.png)

### 面板标题

使用 **.panel-heading** class 可以很简单地向面板添加标题容器

使用带有 **.panel-title** class 的 <h1>-<h6> 来添加预定义样式的标题

![image-20201204132304827](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204132304827.png)

### 面板脚注

把按钮或者副文本放在带有 class **.panel-footer** 的 <div> 中即可

![image-20201204132444105](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204132444105.png)

### 面板带语境色彩

使用语境状态类 **panel-primary、panel-success、panel-info、panel-warning、panel-danger**，来设置带语境色彩的面板

![image-20201204132614621](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204132614621.png)

![image-20201204132630475](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204132630475.png)

### 面板带表格

为了在面板中创建一个无边框的表格，我们可以在面板中使用 class **.table**。

带额外边框分隔， <div>包含<div class="panel-body">

不带边框分割，不包含<div class="panel-body">

![image-20201204133147661](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204133147661.png)

![image-20201204133202898](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204133202898.png)

### 面板带列表组

![image-20201204133303951](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204133303951.png)

![image-20201204133320671](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204133320671.png)

## 十八、插件

通过 data 属性 API 就能使用所有的 Bootstrap 插件

关闭 data 属性 API 的方法，$(document).off('.data-api')

如需关闭一个特定的插件，只需要在 data-api 命名空间前加上该插件的名称作为命名空间，$(document).off('.alert.data-api')

## 十九、模态框

用法：

**通过 data 属性**：设置属性 **data-toggle="modal"**，同时设置 **data-target="#identifier"**

**通过 JavaScript**：使用这种技术，您可以通过简单的一行 JavaScript 来调用带有 id="identifier" 的模态框，`$('#identifier').modal(options)`

options = ‘toggle’/'show'/'hide'  手动切换模态框/手动打开模态框/手动隐藏模态框

**通过事件：**

| show.bs.modal   | 在调用 show 方法后触发。                              | `$('#identifier').on('show.bs.modal', function () {  // 执行一些动作... })` |
| --------------- | ----------------------------------------------------- | ------------------------------------------------------------ |
| shown.bs.modal  | 当模态框对用户可见时触发（将等待 CSS 过渡效果完成）。 | `$('#identifier').on('shown.bs.modal', function () {  // 执行一些动作... })` |
| hide.bs.modal   | 当调用 hide 实例方法时触发。                          | `$('#identifier').on('hide.bs.modal', function () {  // 执行一些动作... })` |
| hidden.bs.modal | 当模态框完全对用户隐藏时触发。                        | `$('#identifier').on('hidden.bs.modal', function () {  // 执行一些动作... })` |

![image-20201204145103263](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204145103263.png)

![image-20201204145134445](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204145134445.png)

## 二十、下拉菜单

**用法：**

**通过 data 属性**：向链接或按钮添加 **data-toggle="dropdown"** 来切换下拉菜单

```html
<div class="dropdown">
  <a data-toggle="dropdown" href="#">下拉菜单（Dropdown）触发器</a>
  <ul class="dropdown-menu" role="menu" aria-labelledby="dLabel">
    ...
  </ul>
</div>
```

**通过 JavaScript**：

```javascript
$('.dropdown-toggle').dropdown()
```

## 二十一、滚动监听

**用法：**

**通过 data 属性**：

向您想要监听的元素（通常是 body）添加 **data-spy="scroll"**。然后添加带有 Bootstrap **.nav** 组件的父元素的 ID 或 class 的属性 **data-target**

**通过JavaScript：**

```javascript
$('body').scrollspy({ target: '.navbar-example' })
```

```
当通过 JavaScript 调用 scrollspy 方法时，您需要调用 .refresh 方法来更新 DOM
$('[data-spy="scroll"]').each(function () {
  var $spy = $(this).scrollspy('refresh')
})
```

```html
<nav id="navbar-example" class="navbar navbar-default navbar-static" role="navigation">
    <div class="container-fluid"> 
    <div class="navbar-header">
        <button class="navbar-toggle" type="button" data-toggle="collapse"
                data-target=".bs-js-navbar-scrollspy">
            <span class="sr-only">切换导航</span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
        </button>
        <a class="navbar-brand" href="#">教程名称</a>
    </div>
    <div class="collapse navbar-collapse bs-js-navbar-scrollspy">
        <ul class="nav navbar-nav">
            <li><a href="#ios">iOS</a></li>
            <li><a href="#svn">SVN</a></li>
            <li class="dropdown">
                <a href="#" id="navbarDrop1" class="dropdown-toggle"
                   data-toggle="dropdown">Java
                    <b class="caret"></b>
                </a>
                <ul class="dropdown-menu" role="menu"
                    aria-labelledby="navbarDrop1">
                    <li><a href="#jmeter" tabindex="-1">jmeter</a></li>
                    <li><a href="#ejb" tabindex="-1">ejb</a></li>
                    <li class="divider"></li>
                    <li><a href="#spring" tabindex="-1">spring</a></li>
                </ul>
            </li>
        </ul>
    </div>
    </div> 
</nav>
<div data-spy="scroll" data-target="#navbar-example" data-offset="0"
     style="height:200px;overflow:auto; position: relative;">
    <h4 id="ios">iOS</h4>
    <p>iOS 是一个由苹果公司开发和发布的手机操作系统。最初是于 2007 年首次发布 iPhone、iPod Touch 和 Apple
        TV。iOS 派生自 OS X，它们共享 Darwin 基础。OS X 操作系统是用在苹果电脑上，iOS 是苹果的移动版本。
    </p>
    <h4 id="svn">SVN</h4>
    <p>Apache Subversion，通常缩写为 SVN，是一款开源的版本控制系统软件。Subversion 由 CollabNet 公司在 2000 年创建。但是现在它已经发展为 Apache Software Foundation 的一个项目，因此拥有丰富的开发人员和用户社区。
    </p>
    <h4 id="jmeter">jMeter</h4>
    <p>jMeter 是一款开源的测试软件。它是 100% 纯 Java 应用程序，用于负载和性能测试。
    </p>
    <h4 id="ejb">EJB</h4>
    <p>Enterprise Java Beans（EJB）是一个创建高度可扩展性和强大企业级应用程序的开发架构，部署在兼容应用程序服务器（比如 JBOSS、Web Logic 等）的 J2EE 上。
    </p>
    <h4 id="spring">Spring</h4>
    <p>Spring 框架是一个开源的 Java 平台，为快速开发功能强大的 Java 应用程序提供了完备的基础设施支持。
    </p>
    <p>Spring 框架最初是由 Rod Johnson 编写的，在 2003 年 6 月首次发布于 Apache 2.0 许可证下。
    </p>
</div>
```

![image-20201204155144676](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204155144676.png)

### 滚动监听更新：

事件

| 事件                  | 描述                                         | 实例                                                         |
| --------------------- | -------------------------------------------- | ------------------------------------------------------------ |
| activate.bs.scrollspy | 每当一个新项目被滚动监听激活时，触发该事件。 | `$('#myScrollspy').on('activate.bs.scrollspy', function () {  // 执行一些动作... })` |

```html
<nav id="myScrollspy" class="navbar navbar-default navbar-static" role="navigation">
    <div class="container-fluid"> 
    <div class="navbar-header">
        <button class="navbar-toggle" type="button" data-toggle="collapse"
                data-target=".bs-js-navbar-scrollspy">
            <span class="sr-only">切换导航</span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
        </button>
        <a class="navbar-brand" href="#">教程名称</a>
    </div>
    <div class="collapse navbar-collapse bs-js-navbar-scrollspy">
        <ul class="nav navbar-nav">
            <li class="active"><a href="#ios">iOS</a></li>
            <li><a href="#svn">SVN</a></li>
            <li class="dropdown">
                <a href="#" id="navbarDrop1" class="dropdown-toggle"
                   data-toggle="dropdown">
                    Java <b class="caret"></b>
                </a>
                <ul class="dropdown-menu" role="menu"
                    aria-labelledby="navbarDrop1">
                    <li><a href="#jmeter" tabindex="-1">jmeter</a></li>
                    <li><a href="#ejb" tabindex="-1">ejb</a></li>
                    <li class="divider"></li>
                    <li><a href="#spring" tabindex="-1">spring</a></li>
                </ul>
            </li>
        </ul>
    </div>
    </div> 
</nav>
<div data-spy="scroll" data-target="#myScrollspy" data-offset="0"
     style="height:200px;overflow:auto; position: relative;">
    <div class="section">
        <h4 id="ios">iOS<small><a href="#" onclick="removeSection(this);">
                    &times; 删除该部分</a></small>
        </h4>
        <p>iOS 是一个由苹果公司开发和发布的手机操作系统。最初是于 2007 年首次发布 iPhone、iPod Touch 和 Apple
            TV。iOS 派生自 OS X，它们共享 Darwin 基础。OS X 操作系统是用在苹果电脑上，iOS 是苹果的移动版本。</p>
    </div>
    <div class="section">
        <h4 id="svn">SVN<small></small></h4>
        <p>Apache Subversion，通常缩写为 SVN，是一款开源的版本控制系统软件。Subversion 由 CollabNet 公司在 2000 年创建。但是现在它已经发展为 Apache Software Foundation 的一个项目，因此拥有丰富的开发人员和用户社区。</p>
    </div>
    <div class="section">
        <h4 id="jmeter">jMeter<small><a href="#" onclick="removeSection(this);">
                    &times; 删除该部分</a></small>
        </h4>
        <p>jMeter 是一款开源的测试软件。它是 100% 纯 Java 应用程序，用于负载和性能测试。</p>
    </div>
    <div class="section">
        <h4 id="ejb">EJB</h4>
        <p>Enterprise Java Beans（EJB）是一个创建高度可扩展性和强大企业级应用程序的开发架构，部署在兼容应用程序服务器（比如 JBOSS、Web Logic 等）的 J2EE 上。</p>
    </div>
    <div class="section">
        <h4 id="spring">Spring</h4>
        <p>Spring 框架是一个开源的 Java 平台，为快速开发功能强大的 Java 应用程序提供了完备的基础设施支持。</p>
        <p>Spring 框架最初是由 Rod Johnson 编写的，在 2003 年 6 月首次发布于 Apache 2.0 许可证下。</p>
    </div>
</div>
<span id="activeitem" style="color:red;"></span>
<script>
    $(function(){
        removeSection = function(e) {
            $(e).parents(".section").remove();
            $('[data-spy="scroll"]').each(function () {
                var $spy = $(this).scrollspy('refresh')
            });
        }
        $("#myScrollspy").scrollspy();
        $('#myScrollspy').on('activate.bs.scrollspy', function () {
            var currentItem = $(".nav li.active > a").text();
            $("#activeitem").html("目前您正在查看 - " + currentItem);
        })
    });
</script>
<nav id="myScrollspy" class="navbar navbar-default navbar-static" role="navigation">
    <div class="container-fluid"> 
    <div class="navbar-header">
        <button class="navbar-toggle" type="button" data-toggle="collapse"
                data-target=".bs-js-navbar-scrollspy">
            <span class="sr-only">切换导航</span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
        </button>
        <a class="navbar-brand" href="#">教程名称</a>
    </div>
    <div class="collapse navbar-collapse bs-js-navbar-scrollspy">
        <ul class="nav navbar-nav">
            <li class="active"><a href="#ios">iOS</a></li>
            <li><a href="#svn">SVN</a></li>
            <li class="dropdown">
                <a href="#" id="navbarDrop1" class="dropdown-toggle"
                   data-toggle="dropdown">Java
                    <b class="caret"></b>
                </a>
                <ul class="dropdown-menu" role="menu"
                    aria-labelledby="navbarDrop1">
                    <li><a href="#jmeter" tabindex="-1">jmeter</a></li>
                    <li><a href="#ejb" tabindex="-1">ejb</a></li>
                    <li class="divider"></li>
                    <li><a href="#spring" tabindex="-1">spring</a></li>
                </ul>
            </li>
        </ul>
    </div>
    </div>
</nav>
<div data-spy="scroll" data-target="#myScrollspy" data-offset="0"
     style="height:200px;overflow:auto; position: relative;">
    <div class="section">
        <h4 id="ios">iOS<small><a href="#" onclick="removeSection(this);">
                    &times; 删除该部分</a></small>
        </h4>
        <p>iOS 是一个由苹果公司开发和发布的手机操作系统。最初是于 2007 年首次发布 iPhone、iPod Touch 和 Apple
            TV。iOS 派生自 OS X，它们共享 Darwin 基础。OS X 操作系统是用在苹果电脑上，iOS 是苹果的移动版本。</p>
    </div>
    <div class="section">
        <h4 id="svn">SVN<small></small></h4>
        <p>Apache Subversion，通常缩写为 SVN，是一款开源的版本控制系统软件。Subversion 由 CollabNet 公司在 2000 年创建。但是现在它已经发展为 Apache Software Foundation 的一个项目，因此拥有丰富的开发人员和用户社区。</p>
    </div>
    <div class="section">
        <h4 id="jmeter">jMeter<small><a href="#" onclick="removeSection(this);">
                    &times; 删除该部分</a></small>
        </h4>
        <p>jMeter 是一款开源的测试软件。它是 100% 纯 Java 应用程序，用于负载和性能测试。</p>
    </div>
    <div class="section">
        <h4 id="ejb">EJB</h4>
        <p>Enterprise Java Beans（EJB）是一个创建高度可扩展性和强大企业级应用程序的开发架构，部署在兼容应用程序服务器（比如 JBOSS、Web Logic 等）的 J2EE 上。</p>
    </div>
    <div class="section">
        <h4 id="spring">Spring</h4>
        <p>Spring 框架是一个开源的 Java 平台，为快速开发功能强大的 Java 应用程序提供了完备的基础设施支持。</p>
        <p>Spring 框架最初是由 Rod Johnson 编写的，在 2003 年 6 月首次发布于 Apache 2.0 许可证下。</p>
    </div>
</div>
<script>
    $(function(){
        removeSection = function(e) {
            $(e).parents(".section").remove();
            $('[data-spy="scroll"]').each(function () {
                var $spy = $(this).scrollspy('refresh')
            });
        }
        $("#myScrollspy").scrollspy();
    });
</script>
```

![image-20201204164713873](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204164713873.png)

#### 滚动水平监听：

```html
<html>
<head>
	<meta charset="utf-8">
	<title>Bootstrap Example</title>
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<link rel="stylesheet" href="https://cdn.staticfile.org/twitter-bootstrap/3.3.7/css/bootstrap.min.css">
	<script src="https://cdn.staticfile.org/jquery/2.1.1/jquery.min.js"></script>
	<script src="https://cdn.staticfile.org/twitter-bootstrap/3.3.7/js/bootstrap.min.js"></script>
	<style>
		body {
			position: relative; 
		}
		#section1 {padding-top:50px;height:500px;color: #fff; background-color: #1E88E5;}
		#section2 {padding-top:50px;height:500px;color: #fff; background-color: #673ab7;}
		#section3 {padding-top:50px;height:500px;color: #fff; background-color: #ff9800;}
		#section41 {padding-top:50px;height:500px;color: #fff; background-color: #00bcd4;}
		#section42 {padding-top:50px;height:500px;color: #fff; background-color: #009688;}
	</style>
</head>
<body data-spy="scroll" data-target=".navbar" data-offset="50">

<nav class="navbar navbar-inverse navbar-fixed-top">
	<div class="container-fluid">
		<div class="navbar-header">
			<button type="button" class="navbar-toggle" data-toggle="collapse" data-target="#myNavbar">
				<span class="icon-bar"></span>
				<span class="icon-bar"></span>
				<span class="icon-bar"></span>                        
			</button>
			<a class="navbar-brand" href="#">WebSiteName</a>
		</div>
		<div>
			<div class="collapse navbar-collapse" id="myNavbar">
				<ul class="nav navbar-nav">
					<li><a href="#section1">Section 1</a></li>
					<li><a href="#section2">Section 2</a></li>
					<li><a href="#section3">Section 3</a></li>
					<li class="dropdown"><a class="dropdown-toggle" data-toggle="dropdown" href="#">Section 4 <span class="caret"></span></a>
						<ul class="dropdown-menu">
							<li><a href="#section41">Section 4-1</a></li>
							<li><a href="#section42">Section 4-2</a></li>
						</ul>
					</li>
				</ul>
			</div>
		</div>
	</div>
</nav>    

<div id="section1" class="container-fluid">
	<h1>Section 1</h1>
	<p>Try to scroll this section and look at the navigation bar while scrolling! Try to scroll this section and look at the navigation bar while scrolling!</p>
	<p>Try to scroll this section and look at the navigation bar while scrolling! Try to scroll this section and look at the navigation bar while scrolling!</p>
	</div>
	<div id="section2" class="container-fluid">
		<h1>Section 2</h1>
		<p>Try to scroll this section and look at the navigation bar while scrolling! Try to scroll this section and look at the navigation bar while scrolling!</p>
		<p>Try to scroll this section and look at the navigation bar while scrolling! Try to scroll this section and look at the navigation bar while scrolling!</p>
	</div>
	<div id="section3" class="container-fluid">
		<h1>Section 3</h1>
		<p>Try to scroll this section and look at the navigation bar while scrolling! Try to scroll this section and look at the navigation bar while scrolling!</p>
		<p>Try to scroll this section and look at the navigation bar while scrolling! Try to scroll this section and look at the navigation bar while scrolling!</p>
	</div>
	<div id="section41" class="container-fluid">
		<h1>Section 4 Submenu 1</h1>
		<p>Try to scroll this section and look at the navigation bar while scrolling! Try to scroll this section and look at the navigation bar while scrolling!</p>
		<p>Try to scroll this section and look at the navigation bar while scrolling! Try to scroll this section and look at the navigation bar while scrolling!</p>
	</div>
	<div id="section42" class="container-fluid">
		<h1>Section 4 Submenu 2</h1>
		<p>Try to scroll this section and look at the navigation bar while scrolling! Try to scroll this section and look at the navigation bar while scrolling!</p>
		<p>Try to scroll this section and look at the navigation bar while scrolling! Try to scroll this section and look at the navigation bar while scrolling!</p>
</div>

</body>
</html>
```

![image-20201204165733284](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204165733284.png)

#### 滚动垂直监听：

```html
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title>Bootstrap 实例</title>
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<link rel="stylesheet" href="https://cdn.staticfile.org/twitter-bootstrap/3.3.7/css/bootstrap.min.css">
	<script src="https://cdn.staticfile.org/jquery/2.1.1/jquery.min.js"></script>
	<script src="https://cdn.staticfile.org/twitter-bootstrap/3.3.7/js/bootstrap.min.js"></script>
	<style>
		body {
			position: relative;
		}
		ul.nav-pills {
			top: 20px;
			position: fixed;
		}
		div.col-sm-9 div {
			height: 250px;
			font-size: 28px;
		}
		#section1 {color: #fff; background-color: #1E88E5;}
		#section2 {color: #fff; background-color: #673ab7;}
		#section3 {color: #fff; background-color: #ff9800;}
		#section41 {color: #fff; background-color: #00bcd4;}
		#section42 {color: #fff; background-color: #009688;}

		@media screen and (max-width: 810px) {
			#section1, #section2, #section3, #section41, #section42  {
				margin-left: 150px;
			}
		}
	</style>
</head>
<body data-spy="scroll" data-target="#myScrollspy" data-offset="20">

<div class="container">
	<div class="row">
		<nav class="col-sm-3" id="myScrollspy">
			<div class="container-fluid"> 
			<div class="container-fluid"> 
			<ul class="nav nav-pills nav-stacked">
				<li class="active"><a href="#section1">Section 1</a></li>
				<li><a href="#section2">Section 2</a></li>
				<li><a href="#section3">Section 3</a></li>
				<li class="dropdown">
					<a class="dropdown-toggle" data-toggle="dropdown" href="#">Section 4 <span class="caret"></span></a>
					<ul class="dropdown-menu">
						<li><a href="#section41">Section 4-1</a></li>
						<li><a href="#section42">Section 4-2</a></li>                     
					</ul>
				</li>
			</ul>
			</div>	
			</div>		
		</nav>
		<div class="col-sm-9">
			<div id="section1">    
				<h1>Section 1</h1>
				<p>Try to scroll this section and look at the navigation list while scrolling!</p>
			</div>
			<div id="section2"> 
				<h1>Section 2</h1>
				<p>Try to scroll this section and look at the navigation list while scrolling!</p>
			</div>        
			<div id="section3">         
				<h1>Section 3</h1>
				<p>Try to scroll this section and look at the navigation list while scrolling!</p>
			</div>
			<div id="section41">         
				<h1>Section 4-1</h1>
				<p>Try to scroll this section and look at the navigation list while scrolling!</p>
			</div>      
			<div id="section42">         
				<h1>Section 4-2</h1>
				<p>Try to scroll this section and look at the navigation list while scrolling!</p>
			</div>
		</div>
	</div>
</div>

</body>
</html>
```

![image-20201204165832497](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20201204165832497.png)

## 二十二、标签页Tab







