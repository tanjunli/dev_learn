<!--
 * @Author: xx123 tavillexback@outlook.com
 * @Date: 2024-03-12 22:00:19
 * @LastEditors: xx123 tavillexback@outlook.com
 * @LastEditTime: 2024-03-17 20:17:53
 * @FilePath: \Markdown\html_study_notes.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
# HTML学习笔记  

- **基础元素**  
  1. 完整页面
   ![菜鸟教程](2024-03-12-22-03-32.png)

  2. 链接
     通过标签&lt;a&gt;来定义，例：

     ```text
     <a href="https://www.runoob.com">这是一个链接</a>
     ```

  3. 图像
     通过标签 &lt;img&gt; 来定义,例:

     ```text
     <img src="/images/logo.png" width="258" height="39" />
     ```

     ***注意： 图像的名称和尺寸是以属性的形式提供的。***

  4. 换行  
     通过标签&lt;br&gt;来定义  
     ***注意：&lt;br&gt; 就是没有关闭标签的空元素。***

  5. 水平线  
     &lt;hr&gt; 标签在 HTML 页面中创建水平线。
  
  6. 注释  
     浏览器会忽略注释，也不会显示它们。例：  

     ```text
     <!-- 这是一个注释 -->
     ```

     ***注释***: 开始括号之后（左边的括号）需要紧跟一个叹号 ! (英文标点符号)，结束括号之前（右边的括号）不需要。

     ***HTML 提示 - 如何查看源代码***  
      只需要单击右键，然后选择"查看源文件"（IE）或"查看页面源代码"（Firefox），其他浏览器的做法也是类似的。这么做会打开一个包含页面 HTML 代码的窗口。

- **文本格式化**  
  1. 文本格式化标签

     |标签|描述|
     |:-:|:-:|
     |&lt;b&gt;|定义粗体文本|
     |&lt;em&gt;|定义着重文字|
     |&lt;i&gt;|定义斜体字|
     |&lt;small&gt;|定义小号字|
     |&lt;strong&gt;|定义加重语气|
     |&lt;sub&gt;|定义下标字|
     |&lt;sup&gt;|定义上标字|
     |&lt;ins&gt;|定义插入字|
     |&lt;del&gt;|定义删除字|

  2. "计算机输出" 标签

     |标签|描述|
     |:-:|:-:|
     |&lt;code&gt;|定义计算机代码|
     |&lt;kbd&gt;|定义键盘码|
     |&lt;samp&gt;|定义计算机代码样本|
     |&lt;var&gt;|定义变量|
     |&lt;pre&gt;|定义预格式样本|

  3. 引文, 引用, 及标签定义

     |标签|描述|
     |:-:|:-:|
     |&lt;abbr&gt;|定义缩写|
     |&lt;address&gt;|定义地址|
     |&lt;bdo&gt;|定义文字方向|
     |&lt;blockquote&gt;|定义长的引用|
     |&lt;q&gt;|定义短的引用语|
     |&lt;cite&gt;|定义引用、引证|
     |&lt;dfn&gt;|定义一个定义项目|

- **链接**  
  1. 文本链接:使用 &lt;a&gt; 元素将一段文本转化为可点击的链接，例如：

     ```text
       <a href="https://www.example.com">访问示例网站</a>
     ```

  2. 图像链接:在这种情况下，&lt;a&gt; 元素包围着 &lt;img&gt; 元素。例如：

     ```text
     <a href="https://www.example.com">
     <img src="example.jpg" alt="示例图片">
     </a>
     ```

  3. 锚点链接:在同一页面内创建内部链接。需要在目标位置使用 &lt;a&gt; 元素定义一个标记，并使用#符号引用该标记。例如：

     ```text
     <a href="#section2">跳转到第二部分</a>
     <!-- 在页面中的某个位置 -->
     <a name="section2"></a>
     ```

  4. 下载链接：如果您希望链接用于下载文件而不是导航到另一个网页，可以使用 download 属性。例如：

     ```text
     <a href="document.pdf" download>下载文档</a>
     ```

  <span style="font-size: larger; font-weight: bold;">链接 - target 属性</span>

    使用 target 属性，你可以定义被链接的文档在何处显示。下面的这行会在新窗口打开文档:

     ```text
     <a href="https://www.runoob.com/" target="_blank" rel="noopener noreferrer">访问菜鸟教程!</a>
     ```

  <span style="font-size: larger; font-weight: bold;">链接- id 属性</span>

     id 属性可用于创建一个 HTML 文档书签。  
     ***提示***: 书签不会以任何特殊方式显示，即在 HTML 页面中是不显示的，所以对于读者来说是隐藏的。  
     ***实例:***  
     在HTML文档中插入ID:

     ```text
     <a id="tips">有用的提示部分</a>
     ```

     在HTML文档中创建一个链接到"有用的提示部分(id="tips"）"：  

     ```text
     <a href="#tips">访问有用的提示部分</a>
     ```

     或者，从另一个页面创建一个链接到"有用的提示部分(id="tips"）"：

     ```text
     <a href="https://www.runoob.com/html/html-links.html#tips">
     访问有用的提示部分</a>
     ```

  ***注释***： 请始终将正斜杠添加到子文件夹。假如这样书写链接：href="<https://www.runoob.com/html">，就会向服务器产生两次 HTTP 请求。这是因为服务器会添加正斜杠到这个地址，然后创建一个新的请求，就像这样：href="<https://www.runoob.com/html/">。

- **头部元素**  

     |标签|描述|
     |:-:|:-:|
     |&lt;head&gt;|定义文档的信息|
     |&lt;title&gt;|定义文档的标题|
     |&lt;base&gt;|定义页面链接标签的默认链接地址|
     |&lt;link&gt;|定义一个文档和外部资源之间的关系|
     |&lt;meta&gt;|定义HTML文档中的元数据|
     |&lt;script&gt;|定义客户端的脚本文件|
     |&lt;style&gt;|定义HTML文档的样式文件|

  1. &lt;head&gt;元素  
     &lt;head&gt; 元素包含了所有的头部标签元素。在 &lt;head&gt;元素中你可以插入脚本（scripts）, 样式文件（CSS），及各种meta信息。
  2. &lt;title&gt;元素  
     - 定义了浏览器工具栏的标题。  
     - 当网页添加到收藏夹时，显示在收藏夹中的标题。
     - 显示在搜索引擎结果页面的标题。
  3. &lt;base&gt;元素  
  &lt;base&gt; 标签描述了基本的链接地址/链接目标，该标签作为HTML文档中所有的链接标签的默认链接:

     ```text
     <head>
     <base href="http://www.runoob.com/images/" target="_blank">
     </head>
     ```

  4. &lt;link&gt;元素  
  &lt;link&gt; 标签定义了文档与外部资源之间的关系。  
  &lt;link&gt; 标签通常用于链接到样式表:

     ```text
     <head>
     <link rel="stylesheet" type="text/css" href="mstyle.css">
     </head>
     ```

  5. &lt;style&gt;元素  
     &lt;style&gt; 标签定义了HTML文档的样式文件引用地址。  
     在&lt;style&gt; 元素中你也可以直接添加样式来渲染 HTML 文档:

     ```text
     <head>
     <style type="text/css">
     body {
     background-color:yellow;
     }
     p {
     color:blue
     }
     </style>
     </head>
     ```

  6. &lt;meta&gt; 元素  
     为搜索引擎定义关键词:

     ```text
     <meta name="keywords" content="HTML, CSS, XML, XHTML, JavaScript">
     ```

     为网页定义描述内容:

     ```test
     <meta name="description" content="免费 Web & 编程 教程">
     ```

     定义网页作者:

     ```test
     <meta name="author" content="Runoob">
     ```

     每30秒钟刷新当前页面:

     ```test
     <meta http-equiv="refresh" content="30">
     ```

  7. &lt;script&gt; 元素  
   &lt;script&gt;标签用于加载脚本文件，如： JavaScript。

- **样式- CSS**  
  CSS 可以通过以下方式添加到HTML中:

  - 内联样式- 在HTML元素中使用"style" 属性
  - 内部样式表 -在HTML文档头部 &lt;head&gt; 区域使用&lt;style&gt; 元素包含CSS
  - 外部引用 - 使用外部 CSS 文件

  样式标签

     |标签|描述|
     |:-:|:-:|
     |&lt;style&gt;|定义文本样式|
     |&lt;link&gt;|定义资源引用地址|

  1. 内联样式
      当特殊的样式需要应用到个别元素时，就可以使用内联样式。 使用内联样式的方法是在相关的标签中使用样式属性。样式属性可以包含任何 CSS 属性。以下实例显示出如何改变段落的颜色和左外边距。

      ```test
      <p style="color:blue;margin-left:20px;">这是一个段落。</p>
      ```

  2. 背景颜色
      背景色属性（background-color）定义一个元素的背景颜色：  

      ```test
      <body style="background-color:yellow;">
     <h2 style="background-color:red;">这是一个标题</h2>
     <p style="background-color:green;">这是一个段落。</p>
     </body>
     ```

  3. 字体, 字体颜色 ，字体大小
      可以使用font-family（字体），color（颜色），和font-size（字体大小）属性来定义字体的样式:

      ```test
      <h1 style="font-family:verdana;">一个标题</h1>
     <p style="font-family:arial;color:red;font-size:20px;">一个段落。</p>
     ```

  4. 文本对齐方式
      使用 text-align（文字对齐）属性指定文本的水平与垂直对齐方式：

      ```test
      <h1 style="text-align:center;">居中对齐的标题</h1>
     <p>这是一个段落。</p>
     ```

  5. 内部样式表  
      当单个文件需要特别样式时，就可以使用内部样式表。你可以在&lt;head&gt; 部分通过 &lt;style&gt;标签定义内部样式表:

      ```test
      <head>
     <style type="text/css">
     body {background-color:yellow;}
     p {color:blue;}
     </style>
     </head>
     ```

  6. 外部样式表  
      当样式需要被应用到很多页面的时候，外部样式表将是理想的选择。使用外部样式表，你就可以通过更改一个文件来改变整个站点的外观。

      ```test
      <head>
     <link rel="stylesheet" type="text/css" href="mystyle.css">
     </head>
     ```

- **图像**  
  图像标签

     |标签|描述|
     |:-:|:-:|
     |&lt;img&gt;|定义图像|
     |&lt;map&gt;|定义图像地图|
     |&lt;area&gt;|定义图像地图中的可点击区域|
  1. 源属性（Src）
      要在页面上显示图像，你需要使用源属性（src）。src 指 "source"。源属性的值是图像的 URL 地址。  
      定义图像的语法是：

      ```test
      <img src="url" alt="some_text">
      ```

      URL 指存储图像的位置。如果名为 "pulpit.jpg" 的图像位于 <www.runoob.com> 的 images 目录中，那么其 URL 为 <http://www.runoob.com/images/pulpit.jpg。>

     浏览器将图像显示在文档中图像标签出现的地方。如果你将图像标签置于两个段落之间，那么浏览器会首先显示第一个段落，然后显示图片，最后显示第二段。
  2. Alt属性
      alt 属性用来为图像定义一串预备的可替换的文本。

     替换文本属性的值是用户定义的。

     ```test
     <img src="boat.gif" alt="Big Boat">
     ```

     在浏览器无法载入图像时，替换文本属性告诉读者她们失去的信息。此时，浏览器将显示这个替代性的文本而不是图像。为页面上的图像都加上替换文本属性是个好习惯，这样有助于更好的显示信息，并且对于那些使用纯文本浏览器的人来说是非常有用的。
  3. 设置图像的高度与宽度
      height（高度） 与 width（宽度）属性用于设置图像的高度与宽度。

     属性值默认单位为像素:

     ```test
     <img src="pulpit.jpg" alt="Pulpit rock" width="304" height="228">
     ```

     ***提示***: 指定图像的高度和宽度是一个很好的习惯。如果图像指定了高度宽度，页面加载时就会保留指定的尺寸。如果没有指定图片的大小，加载页面时有可能会破坏HTML页面的整体布局。
  
  ***有用的提示：***  
  - 假如某个 HTML 文件包含十个图像，那么为了正确显示这个页面，需要加载 11 个文件。加载图片是需要时间的，所以我们的建议是：慎用图片。
  - 加载页面时，要注意插入页面图像的路径，如果不能正确设置图像的位置，浏览器无法加载图片，图像标签就会显示一个破碎的图片。
  
