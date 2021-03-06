## href和src的区别
href和src是有区别的，而且是不能相互替换的。我们在可替换的元素上使用src，然而把href用于在涉及的文档和外部资源之间建立一个关系。

* href (Hypertext Reference)（超文本引用）用来建立当前元素和文档之间的链接。常用的有：link、a。
指定网络资源的位置，从而在当前元素或者当前文档和由当前属性定义的需要的锚点或资源之间定义一个链接或者关系。`<link href="style.css" rel="stylesheet" />`浏览器明白当前资源是一个样式表，页面解析不会暂停（由于浏览器需要样式规则去画或者渲染页面，渲染过程可能会被被暂停）。这与把css文件内容写在`<style>`标签里不相同，因此建议使用link标签而不是@import来吧样式表导入到html文档里。

* src (Source)属性仅仅 嵌入当前资源到当前文档元素定义的位置。src指向的内容会嵌入到文档中当前标签所在的位置。常用的有：img、script、iframe。
当浏览器找到`<script src="script.js"></script>`在浏览器下载，编译，执行这个文件之前页面的加载和处理会被暂停。这个过程与把js文件放到`<script>`标签里类似。这也是建议把JS文件放到底部加载的原因。当然，img标签页与此类似。浏览器暂停加载直到提取和加载图像。
