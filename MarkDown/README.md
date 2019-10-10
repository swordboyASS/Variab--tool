
- 外层
  - 内层
      - 第三层

1. 第一层
    - 第二层
        - 第三层

- [x]  `- [x] 表示一个小勾`

- [ ]  `- [ ] 表示没有勾`

* `表格中也可以嵌套GFM代码`

|表头|作用|
|--:|--:|
|**111**|*222*|
|222|333|

a.我是好人
b.他是好人
c.你是好人

* `锚点`
# 第一章

* 自动链接
<18200230770@163.com>
<https://www.baidu.com>
https://www.baidu.com


进入虚拟环境:

    pipenv



# Markdown--
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
### <!--这是分界线--> 
## 无序列表
* 1
* 2
* 3
## 有序列表
1. 1
2. 2
3. 3

##  列表嵌套
* 第一项：
    - 第一嵌套
    - 第二嵌套
* 第二项：
    - 第一嵌套
    - 第二嵌套

## 插入图片
![这里面放置图片的代替内容 //就是在图片无法加载（像没有网络的情况下）用于替代](这里面放置图片的url)
<!--最后还可以用引号包住并加上选择性的 'title' 属性的文字,像下面这样-->
<!--![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png "RUNOOB")-->
<!--我在这里插入了一个图片-->
![666？](http://n.sinaimg.cn/translate/587/w395h192/20190403/katQ-hvcmeux8993703.gif)  
直接使用 ![]()的方式无法为图片定义尺寸，就会使用默认的尺寸。
<img herf="http://n.sinaimg.cn/translate/587/w395h192/20190403/katQ-hvcmeux8993703.gif" width="50%" htight="%50">

## 插入链接
[这里面是链接的上层显示](这里面放url)  
:blush:[高级链接教程](http://www.runoob.com/markdown/md-link.html)

* [第一章](#第一章)

## 这里是斜体
_这里也是斜体_
*斜体文字*（值得注意的是：星号后面不能有空格）

**粗体文字**
__这里也是粗体__

***既是斜体也是粗体 ***
___这里也既是斜体也是粗体___

## 表格  
Markdown 制作表格使用 | 来分隔不同的单元格，使用 - 来分隔表头和其他行。
语法格式如下：  

### !表格的第二行必须有：---
|  表头   | 表头  |
|  ----  | ----  |
| 单元格  | 单元格 |
| 单元格  | 单元格 |
### 对齐方式  
我们可以设置表格的对齐方式：  
-: 设置内容和标题栏居右对齐。  
:- 设置内容和标题栏居左对齐。  
:-: 设置内容和标题栏居中对齐。

| 左对齐 | 右对齐 | 居中对齐 |  
| :-----| ----: | :----: |  
| 单元格 | 单元格 | 单元格 |  
| 单元格 | 单元格 | 单元格 |  

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |


## 单行代码  
`用两个符号括起来的就是单行代码的注释`

## 代码框
(```用 ``` 包裹一段代码，并指定一种语言（也可以不指定）：它会保留所有空格和缩进并带有代码高亮````)
<!--像这样写出来可以拥有代码高亮）-->
```c# 
class Car
    {
        public readonly int maxSpeed;
        private int currSpeed;

        public Car( int max )
        {
            maxSpeed = max;
        }
        public Car()
        {

            maxSpeed = 55;
        }
```
    
## 段落  
这是另一个段落  （在上一段话后面跟两个空格然后直接回车开始写下一行，但是这样62和63就是一个段落的与另一种写法的细微区别）  
Markdown 段落没有特殊的格式，直接编写文字就好，段落的换行是使用两个以上空格加上回车。<!---->

这是另一个段落

在上一段后面空出一行才是下一个段落；

## 分割线  
***  
用的最多的就是上面这种写法;

* * *

*****

- - -

----------

## 删除线  
~~这段文字是被删除的~~

## 下划线  
下划线可以通过 HTML 的 <u> 标签来实现：（貌似github不支持）

## 脚注
脚注是对文本的补充说明。  
Markdown 脚注的格式如下:  
[^要注明的文本]  
以下实例演示了脚注的用法：
创建脚注格式类似这样 [^RUNOOB]。

[^RUNOOB]: 菜鸟教程 -- 学的不仅是技术，更是梦想！！！（貌似github不支持）

## 引用  
> 最外层
> > 第一层嵌套
> > > 第二层嵌套  
* 如果要在列表项目内放进区块，那么就需要在 > 前添加四个空格的缩进：
    > 哈哈哈
    > 哈哈哈
    
    
 [emojo大全](https://github.com/guodongxiaren/README/blob/master/emoji.md?tdsourcetag=s_pcqq_aiomsg) 
 
 ## 为标题添加emojo  
 :blush: 像这样的用法就是一个表情；
 [emojo大全](https://github.com/guodongxiaren/README/blob/master/emoji.md?tdsourcetag=s_pcqq_aiomsg) 
 ## :blue_book: 这是一个标题 ##
 
 
想知道更高级的用法请访问：[高级技巧](http://www.runoob.com/markdown/md-advance.html)    
    

## 添加本地图片
:blush: 需要先upload-files上传到自己的库，然后再进行下面的操作

<!--先使用html的方式-->
<img src="./001/0.jpeg">


<!--以上传后文件，复制图片地址来添加图片-->
![萌妹子](https://github.com/swordboyASS/Markdown--/blob/master/001/0.jpeg?raw=true)
    

## 创建一个文件夹存放大量图片(/)











