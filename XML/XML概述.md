* ###  XML 被设计用来传输和存储数据。
* ###  HTML 被设计用来显示数据。
* ###  XML 不是对 HTML 的替代


### XML是什么：
* XML 指可扩展标记语言（EXtensible Markup Language）。
* XML 是一种很像HTML的标记语言。
* XML 的设计宗旨是传输数据，而不是显示数据。
* XML 标签没有被预定义。您需要自行定义标签。 
* XML 被设计为具有自我描述性。


### XML 和 HTML 之间的差异

* XML 不是 HTML 的替代。
* XML 和 HTML 为不同的目的而设计：
* XML 被设计用来传输和存储数据，其焦点是数据的内容。
* HTML 被设计用来显示数据，其焦点是数据的外观。
* HTML 旨在显示信息，而 XML 旨在传输信息。


### XML 不会做任何事情
下面实例是 Jani 写给 Tove 的便签，存储为 XML：
```xml
<note>
<to>Tove</to>
<from>Jani</from>
<heading>Reminder</heading>
<body>Don't forget me this weekend!</body>
</note>
```
上面的这条便签具有自我描述性。它包含了发送者和接受者的信息，同时拥有标题以及消息主体。  
也许这有点难以理解，但是 XML 不会做任何事情。XML 被设计用来结构化、存储以及传输信息。  
它仅仅是包装在 XML 标签中的纯粹的信息。我们需要编写软件或者程序，才能传送、接收和显示出这个文档。  

因为 XML 语言没有预定义的标签,所以所有的标签都是使用者自定义的。

#### XML用途
|||
|:---|:----|
| 1  |   XML 把数据从 HTML 分离 |
|  2 |   XML 简化数据共享 |
|   3|   XML 简化数据传输 |
|   4|   XML 简化平台变更 |
|   5|   XML 使您的数据更有用 |
|   6|   XML 用于创建新的互联网语言 |


### 和HTML相同，XML也是树结构
```XML
<bookstore>
    <book category="COOKING">
        <title lang="en">Everyday Italian</title>
        <author>Giada De Laurentiis</author>
        <year>2005</year>
        <price>30.00</price>
    </book>
    <book category="CHILDREN">
        <title lang="en">Harry Potter</title>
        <author>J K. Rowling</author>
        <year>2005</year>
        <price>29.99</price>
    </book>
    <book category="WEB">
        <title lang="en">Learning XML</title>
        <author>Erik T. Ray</author>
        <year>2003</year>
        <price>39.95</price>
    </book>
</bookstore>
```


### 语法
* XML 文档必须有根元素

* XML 声明   
XML 声明文件的可选部分，如果存在需要放在文档的第一行，如下所示：   
`<?xml version="1.0" encoding="utf-8"?> 指定版本，和编码方式（这里是万国码）`

* ML 标签对大小写敏感  
XML 标签对大小写敏感。标签` <Letter> `与标签` <letter> `是不同的。   
必须使用相同的大小写来编写打开标签和关闭标签：

* XML 属性值必须加引号

```XML
<note date="12/11/2007">  ---必须有引号
<to>Tove</to>
<from>Jani</from>
</note>
```

* 实体引用
在 XML 中，一些字符拥有特殊的意义。  
如果您把字符 "<" 放在 XML 元素中，会发生错误，这是因为解析器会把它当作新元素的开始。  
这样会产生 XML 错误 

在 XML 中，有 5 个预定义的实体引用：

| | | |
|:---|:--|:---|
|`&lt;`|<|less than|
|`&gt;`|>|greater than|
|`&amp;`|&|ampersand|
|`&apos;`|'|apostrophe|
|`&quot;`|"|quotation mark|

注释：在 XML 中，只有字符 "<" 和 "&" 确实是非法的。大于号是合法的，但是用实体引用来代替它是一个好习惯。


### 元素
XML 元素必须遵循以下命名规则：
1. 名称可以包含字母、数字以及其他的字符
2. 名称不能以数字或者标点符号开始
3. 名称不能以字母 xml（或者 XML、Xml 等等）开始
4. 名称不能包含空格

##### 最佳命名习惯
1. 使名称具有描述性。使用下划线的名称也很不错：<first_name>、<last_name>。
2. 名称应简短和简单，比如：<book_title>，而不是：<the_title_of_the_book>。
3. 避免 "-" 字符。如果您按照这样的方式进行命名："first-name"，一些软件会认为您想要从 first 里边减去 name。
4. 避免 "." 字符。如果您按照这样的方式进行命名："first.name"，一些软件会认为 "name" 是对象 "first" 的属性。
5. 避免 ":" 字符。冒号会被转换为命名空间来使用（稍后介绍）。
6. XML 文档经常有一个对应的数据库，其中的字段会对应 XML 文档中的元素。有一个实用的经验，即使用数据库的命名规则来命名 XML 文档中的元素。


### 属性
#### 元素 vs 属性
 ```XML
 <person sex="female">
<firstname>Anna</firstname>
<lastname>Smith</lastname>
</person>

<person>
<sex>female</sex>
<firstname>Anna</firstname>
<lastname>Smith</lastname>
</person>
 ```
我的经验是在 HTML 中，属性用起来很便利，但是在 XML 中，您应该尽量避免使用属性。如果信息感觉起来很像数据，那么请使用元素吧。


#### 避免 XML 属性？
因使用属性而引起的一些问题：  
1. 属性不能包含多个值（元素可以）
2. 属性不能包含树结构（元素可以）
3. 属性不容易扩展（为未来的变化）
4. 属性难以阅读和维护。请尽量使用元素来描述数据。而仅仅使用属性来提供与数据无关的信息。

不要做这样的蠢事（这不是 XML 应该被使用的方式）：
```xml
<note day="10" month="01" year="2008"
to="Tove" from="Jani" heading="Reminder"
body="Don't forget me this weekend!">
</note>
```

#### 针对元数据的 XML 属性
有时候会向元素分配 ID 引用。这些 ID 索引可用于标识 XML 元素，它起作用的方式与 HTML 中 id 属性是一样的。这个实例向我们演示了这种情况：
```xml
<messages>
<note id="501">
<to>Tove</to>
<from>Jani</from>
<heading>Reminder</heading>
<body>Don't forget me this weekend!</body>
</note>
<note id="502">
<to>Jani</to>
<from>Tove</from>
<heading>Re: Reminder</heading>
<body>I will not</body>
</note>
</messages>
```
上面的 id 属性仅仅是一个标识符，用于标识不同的便签。它并不是便签数据的组成部分。   
在此我们极力向您传递的理念是：元数据（有关数据的数据）应当存储为属性，而数据本身应当存储为元素。



### 使用XSLT
XSLT可以将XML文档转换成XML格式。

























































































































































































































































