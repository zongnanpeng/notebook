# HTML

本文是一篇HTML入门的笔记，一共有四个部分组成:

* 元素
* 多媒体
* 嵌入
* 表格
* 表单

---

## HTML元素

本模块主要讲述HTML语法和元素的基础知识，包括以下小节：

* 元素认知
* 文档结构元素
* 文字处理元素
* 网页架构元素

---

### 1. 元素认知

元素组成：由标签(tag)、属性（attribute)、内容（content）组成

元素分类：

* 块级元素：出现在新的一行，用于展现结构化内容，比如段落，列表，导航菜单，页脚等
* 内联元素：用于包裹文字

实体化字符：`<` ==> `&lt`; `> ==> &gt;`; `" ==> &quot;`; `' ==> &apos;`; `& ==> &amp;`。

---

### 2. 文档结构元素

 `<!DOCTYPE html>`：声明文档类型，在现代WEB中没有实际作用。

 `<html></html>`：包含了整个页面的内容， 被称为根元素。

`<head></head>`：包含一些页面设置和资源，比如面向搜索引擎的搜索关键字， 页面描述， 字符编码，样式表资源，内部包含`<title></title> <meta> <link>`等标签

`<meta>`：提供元数据(metadata), 用于描述和设置html document。

>组成：http-equiv => 主要用于描述http信息。name => 主要设置文档信息。
>
>name属性：
>
> * 作用：主要用于描述网页
> * keywords: 告诉搜索引擎网页的关键字。
> * description: 网站描述。
> * viewport: 移动端的窗口。content 的值为：width=deivce-width;initial-scale=1
>
> http-equiv属性:
>
> * 作用：主要用于设置http。
> * content-type: 设置网页字符集。content=“text/html;charset=utf-8”;H5推荐使用 charset="utf-8"。
> * X-UA-Compatible: 设置浏览器版本，默认最新版本,比如chrome=1; 常规配置为content = "IE=edge"。
> * cache-control: 缓存控制，值为：no-cache=>发送请求，若资源未更改则使用缓存; no-store=>禁用缓存;maxage:=>设置缓存生命时长，为0则等价于禁用缓存。

`<title></title>`：作用：设置页面的标题，浏览器收藏网页的描述性文字。

`<body></body>`：向用户展示的内容

---

### 3. 文字处理元素

图像：

* 形式： `<img src="图片的地址" alt="图片的描述性文字"`
* src：图片的地址。
* alt: 图片未正常加载时显示给用户的解释性文字。

标题：h1 ~ h6， 一共六级标题，h1为主标题，在文档中允许初选一次。章h1  节 h2  段 h3

段落(Paragraph):指定段落

列表:

* 无序列表(Unlodered List)：`<ul></ul>`
* 有序列表(Ordered List)：`<ol></ol>`
* 列表元素 `<li></li>`

链接：`<a></a>`(Anchor)(锚) ，属性有：

* href (hypertext reference) (超文本引用): 链接的地址，需要加`http(s)://`,也可以链接到相同文档的文档片段。
* download:  文件下载名，设置该属性用于下载网络文件。用于发送邮件：href="mailto:example@qq.com"
* target: 设置新链接打开的位置, _blank设置为在新的窗口打开链接

斜体：em

粗体: strong

下划线：u

描述列表：dl(description list, 列表容器), dt( description term,描述术语 )， dd( description description， 描述内容)

缩略语：abbr，设置title属性用于对缩略语进行解释

联系方式：address，标记联系方式。

上标和下标：sup（上标 ）;sub(下标)。

时间：time，设置时间显示方式, datetime属性中放入正确的时间格式。

---

### 3. 文档与网页架构

图示:

![picture](../images/snapshot.png)

结构:

* 标题栏：横跨整个页面顶部的大标题，通常存在于所有网页。
* 导航栏：指向网站各个区段的超链接，导航栏通常在所有网页中保持一致，可以单独成行，也可以放在标题栏中。
* 主内容：中心大部分区域是网站的独有内容，比如视频，文章，地图，新闻等。
* 侧边栏：外围信息，比如引用，广告，辅助导航系统等。
* 页脚：横跨页面底部的区域，放置公共信息，一般使用较小字体，且为次要内容。

元素:

* header:用于标题栏,内容常用h1元素
* nav: 导航栏。内容多为被列表元素包括的链接元素和用于搜索的表单元素
* main: 主内容，内部通常分各类区段，如article,section ,div 等元素
* aside: 侧边栏,通常放置在main元素中
* footer: 页脚,通常为小字体的次要内容  

代码示例:

            <header>
            <h1>Header</h1>
            </header>
            <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Our team</a></li>
                <li><a href="#">Projects</a></li>
                <li><a href="#">Contact</a></li>
            </ul>`
           <form>
                <input type="search" name="q" placeholder="Search query">
                <input type="submit" value="Go!">
            </form>
            </nav>

            <main>

            <article>
                <section>
                    <h2>Article heading</h2>
                    <p></p>
                </section>
                <section>
                        <h3>Subsection</h3>
                        <p></p>
                        <p></p>
                </section>
                <section>  
                    <h3>Another subsection</h3>
                    <p> </p>
                    <p></p>
                </section>
            </article>

            <aside>
                <h2>Related</h2>

                <ul>
                <li><a href="#">Oh I do like to be beside the seaside</a></li>
                <li><a href="#">Oh I do like to be beside the sea</a></li>
                <li><a href="#">Although in the North of England</a></li>
                <li><a href="#">It never stops raining</a></li>
                <li><a href="#">Oh well...</a></li>
                </ul>
            </aside>

            </main>

            <footer>
            <p>©Copyright 2050 by nobody. All rights reversed.</p>
            </footer>

        </body>
        </html>

---

## 多媒体

网页内容主要由文字和多媒体资源组成，基础内容主要介绍网页结构和文字排版元素，本章节主要介绍多媒体元素，多媒体资源包括图片、视频、音频、矢量图、其他网页等，该类型元素又被称为替换元素，因为它们的内容和尺寸有外部资源所定义。

本章主要包括以下四小节：

* 图片
* 视频和音频
* 嵌入技术
* 矢量图

---

### 1. 图片

元素：img，

属性：

* src: source, 多媒体资源的路径。
* alt: 用于图片无法显示时的替代内容。
* width/height: 用于设置图片容器的大小， 不推荐使用。
* title：用于鼠标悬浮时的解释性文字。 

提示性工具：`<figure>  <img> <figcaption>说明性文字</figcaption> </figure>`。

背景图片：css设置， background-image: url("")。

响应时图片：略。

---

### 2. 音频和视频

video元素用于控制视频播放，属性有：

* src：source, 多媒体资源的地址。
* controls:布尔属性， 用于向用户开放控制视频播放的按钮，可在js中的API中进行控制。建议加上。
* width/height: 设置播放器的宽度和高度。
* autoplay:布尔属性， 自动播放，不建议设置。
* loop: 布尔属性，自动循环播放，不建议使用。
* muted: 布尔熟悉，播放视频时默认关闭声音。
* poster: 属性值为图片的地址，用于覆盖视频。
* preload: 视频缓存控制。 none -- 不缓存；auto -- 页面加载完成后缓存; metadata -- 仅缓存元数据。

audio元素用于控制音频播放，属性和用法同于video。但是没有width/height 和poster视觉属性。

播放格式兼容性处理：

`<video controls><source src="video.mp4" type="video/mp4">`
`<source src="video.webm" type="video/ \webm<p>您的播放器无法播放该媒体资源</p>`
`</video>`

视频和音频都适用。

字幕（适用于视频和音频）: 暂时不使用。

---

### 矢量图

图片的分类：

* 位图： 由像素点构成，比如*.bmp, *.png, *.jpg, *.gif等，放大时会失真。
* 矢量图: *.svg文件，通过算法获得,不会造成失真。

---

## 嵌入技术

历史: frame/framset、object、embed --> iframe、canvas、video、autio

iframe属性:

* allowfullscreen: 布尔属性，允许通过JS设置全屏模式。
* src: 多媒体资源。
* sandbox: 可以为布尔属性，此时为默认设置，用于隔离框架可父页面的信息交流，提高安全性。

处理安全隐患:

* 设置sandbox属性
* 使用https服务
* 配置CSP指令

---

## HTML表格

### 基础

1. 定义：由行和列组成的结构化数据集。
2. 特点：严格。
3. 表格的默认大小是根据其内容定的。
4. 元素：
    * table:表格
    * td: （table data）, 表格数据，单元格
    * tr： (table row),表格的行
    * th: (table header),表格的头部，列标题
    * caption: 表格标题，位于table元素内
    * thead: 表头
    * tbody: 表体
    * tfoot: 表脚
5. colspan: 设置单元格占有n列单元格的宽度
6. rowspan: 设置单元格占有n行单元格的高度
7. 列样式：col元素包含在colgroup容器中,colgroup位于table容器的首位,每一个col元素代表一列的占位，每列的样式在对应的col元素上设置
8. scope: th元素的属性，用于关联多行或者多列,便于屏幕阅读器识别

---

## 表单

该模块主要介绍表格时使用。

表格主要用于和用户进行交互，收集用户提交的信息。

该模块主要包括以下部分：

* 表单基础
* 原生表单挂件
* 发送表单数据
* 表单验证
* 自定义表单挂件
* 通过js发送表单
* 样式化表单
* 表单的高级设置
* 表单挂件的正确兼容表格

---

### 表单元素

1. form: 表单
2. fieldset: 表单区块，常与legend元素一起使用
3. legend: 域说明元素,内嵌于fieldset容器中
4. label: 小部件的辅助标签
5. p标签包裹输入组件和标签，是组件结构化

### 通用属性

1. autofocus: 默认false，自动聚焦，每个页面允许一个
2. disabled: 使组件失效
3. form：绑定父级表单
4. name/ value：元素的name和value

### 输入文本域

1. 特点: 可以被标记 readonly、placeholder、size和patten(拼写检查)
2. 单行文本域:input，默认值在value中
3. 多行文本域: textarea, 默认值写在标签内

### 表单数据校验

1. 校验的方式：

    * JS校验
    * html校验

### 表单元素的设计问题

1. 使用box-sizing属性使元素等宽
2. textarea是inline-block,通常与标签底部对齐，因此设置 vertical-align:top，顶部对齐。
