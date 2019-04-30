# HTML

## 概览

1. ### H5新增标签

    >#### 区块标签：
    >* **header**: 定义标题栏。
    >* **nav**: 定义导航栏。
    >* **main**:  定义主要内容。
    >* **article**: 定义文章。
    >* **section**: 定义文章区块。
    >* **aside**: 定义侧边栏。
    >* **footer**:　定义文章底栏。

    >#### 表单增强：
    >* 日期，时间，搜索，邮箱，数字等
    >* 表单验证
    >* 自动聚焦

2. ### 基础知识

    >#### 元素（`element`)    
    >由开始标签(`<tag>`)内容和结束标签(`</tag>`)组成,并且具有自己的属性(*attribute*)。

## 标签

1. ### 文档结构
    >#### `<!DOCTYPE html>`
    >声明文档类型，在现代WEB中没有实际作用

    >#### `<html></html>`    
    >包含了整个页面的内容， 被称为根元素。

    >#### `<head></head>`
    >包含一些页面设置和资源，比如面向搜索引擎的搜索关键字， 页面描述， 字符编码，样式表资源，内部包含`<title></title> <meta> <link>等标签`

    > #### `<meta>`   
    >作用：提供元数据(metadata), 用于描述和设置html document。  
    >组成：http-equiv => 主要用于描述http信息。name => 主要设置文档信息。     
    >name属性：    
    >* 作用：主要用于描述网页。    
    >* keywords: 告诉搜索引擎网页的关键字。   
    >* description: 网站描述。
    >* viewport: 移动端的窗口。content 的值为：width=deivce-width;initial-scale=1  
    >     
    >http-equiv属性:  
    >* 作用：主要用于设置http。  
    >* content-type: 设置网页字符集。content=“text/html;charset-utf-8”;H5推荐使用 charset="utf-8"。
    >* X-UA-Compatible: 设置浏览器版本，默认最新版本,比如chrome=1; 常规配置为content = "IE=edge"。
    >* cache-control: 缓存控制，值为：no-cache=>发送请求，若资源未更改则使用缓存; no-store=>禁用缓存;maxage:=>设置缓存生命时长，为0则等价于禁用缓存。

    >#### `<title></title>`
    >设置页面的标题，浏览器收藏网页的描述性文字。

    >#### `<body></body>`
    >向用户展示的内容

2. ### 图像    
    > #### `<img src="图片的地址" alt="图片的描述性文字"`        
    > src：图片的地址。    
    > alt: 图片未正常加载时显示给用户的解释性文字。
3. ### 标记文本
    >#### 标题(Heading)
    >共有六级标题 h1 ~ h6

    >#### 段落(Paragraph)    
    >指定段落

    >#### 列表
    >* 无序列表(Unlodered List)：`<ul></ul>`
    >* 有序列表(Ordered List)：`<ol></ol>`
    >* 列表元素 `<li></li>`
4. ### 链接
    >#### `<a></a>`  
    >元素: (Anchor)(锚)  
    >href (hypertext reference) (超文本引用): 链接的地址，需要加`http(s)://`
