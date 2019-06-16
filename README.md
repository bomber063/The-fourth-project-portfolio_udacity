# The-fourth-project-portfolio_udacity
## 第一次提交的问题
很可能是使用了中文命名，不推荐这样，因为在不同的计算机系统的编码解码方式有所不同，同一个中文字可能会得到不同的结果。

为此，都推荐用英文或拼音来命名文件夹、文件的名称。

.txt 文件也建议改用 UTF-8 编码，否则在很多系统下也会是乱码。如下方法可能值得参考：

* [windows环境下新建.txt文件，使其默认以UTF-8编码 - CSDN博客](https://blog.csdn.net/longintchar/article/details/61623130)  
另外，CSS 的 id 或 class 名称也都建议用英文或拼音，非常不推荐用中文。  

## 第二次提交的html文件说明
### 棒极了
html文件第五行代码   
很棒！添加 viewport <meta> 标签，为响应式布局做好准备！  

## 建议修改
代码第14行
<h#> 标签中不推荐包裹其他标签，此处的 ul 就不应该被h1标签包裹：
![图片](https://udacity-reviews-uploads.s3.us-west-2.amazonaws.com/_attachments/31632/1531701813/comp.png)

## 语义化
代码第21行  
使用语义标签来使得整个 HTML 更加容易理解，很棒的做法 👍  
推荐阅读 📚：  
介绍了各个语义标签和一些前端的知识  
* [Semantic HTML](http://justineo.github.io/slideshows/semantic-html/#/)  
深入的思考和理解  
* [关于语义化 HTML 以及前端架构的一点思考](https://www.oschina.net/translate/about-html-semantics-front-end-architecture)  
知乎的一个回答    
* [如何理解 Web 语义化？](https://www.zhihu.com/question/20455165)    

## 需要修改
代码第22行
虽然size属性仍然得到所有主流浏览器的支持，但size属性是HTML5中被淘汰了的属性，不能使用：  
![图片](https://udacity-reviews-uploads.s3.us-west-2.amazonaws.com/_attachments/31632/1531701956/comp.png)  
你可以用CSS样式中的height来代替，另外width和color也是同样的问题，请编写在样式表中：  
```
hr {
   height: 30px;
   width: 100%;
   color: red;
}
```
### 棒极了
第104行代码  
熟练使用了表格，👍  

## styles.css文件说明
### 第11行代码建议
推荐 } 顶格写  

### 第13行代码建议
#### 建议
代码品质 🔬  
根据 [Udacity 前端 CSS 代码风格: 属性名标点](https://github.com/udacity/frontend-nanodegree-styleguide-zh/blob/master/%E5%89%8D%E7%AB%AF%E5%B7%A5%E7%A8%8B%E5%B8%88%E7%BA%B3%E7%B1%B3%E5%AD%A6%E4%BD%8D%E6%A0%B7%E5%BC%8F%E6%8C%87%E5%8D%97%20-%20CSS.md#%E5%B1%9E%E6%80%A7%E5%90%8D%E6%A0%87%E7%82%B9) :  

> 所有属性名冒号后均需添加空格，但属性和冒号间不加空格，以增加连贯性。  

**不推荐：**  
```font-weight:bold;  
padding : 0;  
margin :0;  
```
**推荐：**  
```
font-weight: bold;  
padding: 0;   
margin: 0;  
```  

### 第16行代码建议
#### 建议
代码品质 🔬
根据 [Udacity 前端 CSS 代码风格: 声明区标点](https://github.com/udacity/frontend-nanodegree-styleguide-zh/blob/master/%E5%89%8D%E7%AB%AF%E5%B7%A5%E7%A8%8B%E5%B8%88%E7%BA%B3%E7%B1%B3%E5%AD%A6%E4%BD%8D%E6%A0%B7%E5%BC%8F%E6%8C%87%E5%8D%97%20-%20CSS.md#%E5%A3%B0%E6%98%8E%E5%8C%BA%E6%A0%87%E7%82%B9) :

> 最后一个选择符和声明区起始处的左大括号之间需加空格。

不推荐：
```
.image{...
}
```
推荐：
```
.image {
    ...
}
```
### 第74行代码建议
#### 建议
* 代码规范：
> 我们建议所有选择符和声明均需另起一行。
不推荐：
```
h1, h2, h3 { 
    font-weight: normal; 
    line-height: 1.2; 
}
```
推荐：
```
h1, 
h2, 
h3 { 
    font-weight: normal; 
    line-height: 1.2; 
}
```
引用：[选择符和声明分隔](https://github.com/udacity/frontend-nanodegree-styleguide-zh/blob/master/%E5%89%8D%E7%AB%AF%E5%B7%A5%E7%A8%8B%E5%B8%88%E7%BA%B3%E7%B1%B3%E5%AD%A6%E4%BD%8D%E6%A0%B7%E5%BC%8F%E6%8C%87%E5%8D%97%20-%20CSS.md#%E9%80%89%E6%8B%A9%E7%AC%A6%E5%92%8C%E5%A3%B0%E6%98%8E%E5%88%86%E9%9A%94)

### 三个问题
1. 为什么a标签既定义ID又定义class，有什么特别用处吗？
* 对于标签，我们是可以既给它们定义id又给它们定义class的。在此处，我们定义class是为了筛选出此标签为它设定CSS样式。定义id是为了给它设置JavaScript，添加交互效果。
* 当然，你也可以只设置id或者只设置class。没有一个绝对的标准，按照不同场景灵活处理就好

2. 问题2、这里的svg是什么意思，后面的viewBox="0 0 24 24"的具体描述意义？以及styles中的描述意义？
* 建议遇到没见过的标签或知识时，善用搜索引擎和mdn文档。我在这就不过多介绍了，阅读下方文档了解下svg吧：
* [MDN - SVG](https://developer.mozilla.org/zh-CN/docs/Web/SVG)

3. 问题3、这里的path是什么意思，styles中的path，transform-origin：0px 0px 0px代表什么意义？
* 建议这个问题从属于svg，你可以阅读 [此链接](https://developer.mozilla.org/zh-CN/docs/Web/SVG/Tutorial/Paths) 了解详情~
* p.s. 今后课程当中的类似问题，推荐你在论坛提问，会有咱们的论坛mentor为你详细解答。好处是你的提问今后能够沉淀下来，帮助更多遇到同样困惑的同学~

## 第三次提交的html文件
### 第一个审查
* 棒极了
* 整个 HTML 文档都通过了验证。👍

### 24行代码
* 建议
> 在 [前端工程师纳米学位样式指南 - HTML](https://github.com/udacity/frontend-nanodegree-styleguide-zh/blob/master/%E5%89%8D%E7%AB%AF%E5%B7%A5%E7%A8%8B%E5%B8%88%E7%BA%B3%E7%B1%B3%E5%AD%A6%E4%BD%8D%E6%A0%B7%E5%BC%8F%E6%8C%87%E5%8D%97%20-%20HTML%20.md#html-%E5%BC%95%E5%8F%B7) 有建议指出：
> 在引用属性值时，使用双引号。
> 在编写 HTML 的时候，属性的值都推荐用双引号包含起来。记得为 nav-list 补充一对双引号～

