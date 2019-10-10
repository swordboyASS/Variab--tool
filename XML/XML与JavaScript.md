
<p id="title"></p>

## 目录

:arrow_down:<a href="#01">浏览器对XML DOM的支持</a>

:arrow_down:<a href="#02">浏览器对XPath的支持</a>

:arrow_down:<a href="#03">浏览器对XSLT的支持</a>



<p id="01"></p>

:arrow_double_up:<a href="#title">返回目录</a>

### 浏览器对XML DOM的支持
1. 可以用下面的语法创建一个空的XML文档

`var xmldom=document. implementation. createDocument(namespaceUri, root, doctype);`

创建一个文档元素为<root>的XML文档，null参数是必须的
  
```javascript
  
        var xmldom = document.implementation.createDocument("", "root", null);
        
        alert(xmldom.documentElement.tagName);  //"root"
       
        var child = xmldom.createElement("child");
        xmldom.documentElement.appendChild(child);
```

这个例子创建了一个XMLDOM文档，没有默认的命名空间，也没有文档类型。但要注意的是，尽管不需要指定命名空间和文档类型，也必须传入相应的参数。具体来说，给命名空间URI传入一个空字符串，就意味着未指定`命名空间`，而给文档类型传入nu11，就意味着不指定`文档类型`。变量xmldom中保存着一个DOM2级Document类型的实例，带有第12章讨论过的所有DOM方法和属性。我们这个例子显示了文档元素的标签名，然后又创建并给文档元素添加了一个新的子元素。
要检测浏览器是否支持DOM2级XML，可以使用下面这行代码：

`var hasxm1pom=document.implementation.hasFeature（“XML"，"2.0"）；`

2. DOMParser类型
为了将XML解析为DOM文档，在解析XML之前，首先必须创建一个DoMParser的实例，然后再调用parseFromString（）方法。这个方法接受两个参数：要解析的XML字符串和内容类型（内容类型始终都应该是“text/xm1"）。返回的值是一个Document的实例。来看下面的例子。
```javascript
      var parser=new DoMParser（）；
      var xmldom=parser.parseFromstring（"<root><child/></root>"，"text/xml"）；
      
      alert（xmldom.documentElement.tagName）；//"root"
      alert（xmldom.documentElement.firstChild.tagName）；//"child"
    
      var anotherchild=xmldom.createElement（"child"）；
      xm1dom.documentElement.appendChild（anotherChild）；
      
      var children=xmldom.getElementsByTagName（“child"）；
      alert（children.length）；//2
```
3. XMLSerializer类型
在引入DoMParser的同时，Firefox还引入了XLSerializer类型，提供了相反的功能：将DOM文档序列化为XML字符串。后来，IE9+、Opera、Chrome和Safari都支持了
XMLSerializer。

要序列化DOM文档，首先必须创建XMLSerializer的实例，然后将文档传入其 serializero-
string（）方法，如下面的例子所示。
```javascript
var serializer=new XMLSerializer();
var xml=serializer. serializeTostring(xmldom); 
alert(xml);
```
XMLSerializer可以序列化任何有效的DOM对象，不仅包括个别的节点，也包括HTML文档。  
将HTML文档传入serializerostring（）以后，HTML文档将被视为XML文档，因此得到的代码也将是格式良好的。




<p id="02"></p>

:arrow_double_up:<a href="#title">返回目录</a>

### 浏览器对XPath的支持




<p id="03"></p>

:arrow_double_up:<a href="#title">返回目录</a>

### 浏览器对XSLT的支持




