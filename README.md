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
