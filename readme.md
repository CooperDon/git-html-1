# 《HTML入门笔记1》

### 一、HTML概述

1. 万维网简述

   	+ WWW world wide web
   	+ 本质：内容/资源共享
   	+ URL + HTTP + HTML

2. HTML概述

   HTML的全称为HyperText Markup Language(超文本标记语言)，由爵士李教授在1990创作诞生。

### 二、HTML文档结构简述

1. 文档基本类型及其释义

   ```html
   <!DOCTYPE html>		<!-- 文档类型为HTML，供页面解析时使用 -->
   <html lang="en">	<!-- html标签，lang为其一属性，en表示英文，通常使用zh-CN表示中文简体 -->
   <head>				<!-- html包含head和body两部分 -->
       <!-- 文字/字符的编码格式 -->
       <meta charset="UTF-8">
       <!-- 用IE浏览器打开时，使用最新的IE内核 -->
       <meta http-equiv="X-UA-Compatible" content="IE=edge">
       <!-- 兼容手机时，规定屏幕的大小、是否可缩放 -->
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Document</title>
   </head>
   <body>
       <!-- 添加页面的具体内容 -->
   </body>
   </html>
   ```

2. HTML章节标签(网页的框架)

   #### 内容

   + 标题h1~h6
   + 章节section
   + 文章article
   + 段落p
   + 头部header
   + 底部footer
   + 主要内容main
   + 区域划分div

   #### 练习

   ```html
   <!DOCTYPE html>
   <html>
   <head>
     <meta charset="utf-8">
     <title>JS Bin</title>
   </head>
   <body>
     <header>最后一颗子弹留给我</header>
       <main>
         <h1>一级标题<h1><h2>二级标题<h2><h3>三级标题<h3>
         <h4>四级标题<h4><h5>五级标题<h5><h6>六级标题<h6>
         <section>
           <h2>第一章</h2>
           <p>故事说明</p>
           <section>
             <h3>1.1节</h3>
             <p>第1节内容</p>
           </section>
            <section>
             <h3>1.2节</h3>
             <p>第2节内容</p>
           </section>
         </section>
       </main>
       <aside>
         相似推荐
       </aside>
     <footer>&copy版权声明</footer>
   </body>
   </html>
   ```

   #### 效果

   ![html结构标签](https://i.loli.net/2021/07/31/F37yxlmhWfoCjGT.png)

3. 标签的全局属性

   + id

     + 用法为：#xxx(xxx为标签的id名称)
     + 作用与class相同
     + 慎用id(调用时只能有一个)

   + class

     + 用法为 .middle{}
     + 给选中标签元素添加样式
     + 可以有一个或多个

   + style 

     + 用法为直接在标签内部添加style
     + 内部样式较id、class的优先级最高

   + hidden

     + 隐藏标签内容

   + title

     + 显示完整内容

   + tabindex

     + tabindex 属性规定元素的 tab 键控制次序（当 tab 键用于导航时）。
     + 取值包括："-1"禁止访问，"0"最后访问，"num"顺序访问

   + contenteditable

     + 属性作用：用户是否可以编辑内容

       ```css
       //将style放至body时，给style添加contenteditable属性可使style可编辑用于项目调试，具体代码如下
       <style contenteditable>
           style{display:block; border:1px solid red;}
           .middle {
             background: black;
             color: blanchedalmond;
           }
        </style>
       ```

4. 默认样式

   ###### 步骤

   + 打开浏览器
   + 按F12
   + 选中elements
   + 选中style
   + 查看user agent stylesheet 
   + 选中待查看的标签

   ![Snipaste_2021-07-31_19-27-45](https://i.loli.net/2021/07/31/2fswoKT8WXc4qDO.png)

   ###### 改变默认样式(css reset)

   ```css
   *{
       margin:0;
       padding:0;
       box-sizing:border-box;
   }
   *::after,*::before{
       box-sizing:border-box;
   }
   h1,h2,h3,h4,h5,h6{
       font-weight:normal;
   }
   ul,ol{
       list-style:none;
   }
   a{
       text-decoration:none;
   }
   a:hover{
       text-decoration:underline;
   }
   table{
        border-collapse: collapse;
        border-spacing: 0;
   }
   ```

5. 常见内容标签

   ###### 内容

   + ol + li，ul + li
     + 有序列表
     + 无序列表
   + dl + dt + dd
     + 内容描述，分类加内容
   + pre
     + 将空格、tab等保留
   + hr
     + 下划线
   + br
     + 换行
   + a
     + 超链接
   + em
     + 强调(字体为斜体)
   + strong
     + 重要(字体为加粗)
   + code
     + 代码区域
   + quote
     + 文章中的引用
     + 欧阳修说过：<quote>三上：上、上、上</quote>
   + blockquote
     + 欧阳修说过：<blockquote>三上：上、上、上</blockquote>
     + 同为引用，作用为可换行

   ###### 效果

   ![Snipaste_2021-07-31_20-21-00](https://i.loli.net/2021/07/31/ekQvFhpxtind9r2.png)
