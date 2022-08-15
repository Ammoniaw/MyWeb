HTML（基础）学习之旅

# 不要抱怨自己什么都学不会，那是因为你没有用心

# unit1:HTML

## 1.什么是HTML

## 1.1 HTML的概念

## HTML是超文本编辑语言，是网页的标记语言。HTML不是一种编程语言，而是一门描述性的标记语言

### 1.1.1 语法

```html
<标签符>内容</标签符>
```

### 1.1.2 说明

#### 标签符一般都是成对出现的，包含一个开始符号和结束符号

##### 示例：定义文字为斜体

```html
<em>电视剧《天下第一》</em>
```

### 1.1.3 学习HTML究竟学习什么

#### 学习HTML就是学习各种各样的标签，然后针对自己想要在网页上显示的东西，使用正确的标签

#ps元素即是标签的意思

# unit2: 开发工具

## Hbulider

# unit3:基本标签学习

## 3.1 HTML结构学习

```html
<!DOCTYPE html>
<html>
    <head>
    </head>
    <body>
    </body>
</html>
```

### 1.文档声明

```html
<!DOCTYPE hmtl>
```

#### 上述代码表示这是一个文档声明，表示这是一个HTML页面

### 2.HTML标签

```html
<html>
...
</html>
```

#### html标签的作用就是告诉浏览器这个页面是从< html>开始到< /html>结束的

### 3.head标签

```html
<head>
...
</head>
```

#### < head>< /head>>是网页的头部，用于定义一些特殊的内容

##### 例如：页面标题-定时刷新-头部文件等

```html
<head>
    <title>网页的标题写在这个地方</title>
</head>
```

### 4.body标签

```html
<body>...</body>
```

#### body标签顾名思义是网页的身体，对于一个网页来说，大部分的代码都是在这个标签内部来完成的

<!DOCTYPE html>
<html>
    <head>
    	<meta charset="utf-8"/>
        <title>这是网页的标题部分</title>
    </head>
    <body>
        <p>这是网页的内容</p>
    </body>
</html>

## 3.2 head标签

### 在HTML中一般来说，只有6个标签可以放在head标签中,title;meta;link;style;script;base标签

### 3.2.1 title标签

#### 说明:title标签唯一的作用就是定义网页的标题

```html
<!DOCTYPE doc>
<html>
    <head>
        <meta charset="utf-8"/><!--防止中文网页出现乱码-->
        <title>当前网页的标题</title>
    </head>
    <body></body>
</html>
```

tips:实际开发中，要求在每一个页面上面都要写上title

### 3.2.2 meta标签

#### 在HTML中，meta标签一般用于定义页面的特殊信息，比如页面关键字、页面描述等。这些信息本不是提供给用户看的，而是提供给搜索引擎（百度、谷歌和搜狗等）。简而言之，meta标签就是告诉搜索引擎，这个网页页面是用来干什么的

##### 1.name属性

```html
<!DOCTYPE html>
<html>
    <head>
        <meta name="keywords" content="描述网页的关键字">
        <meta name=description content="网页描述，网页是用来干什么的"/>
        <meta name="author" content="描述网页的作者信息"/>
        <meta name="copyright" content="网页的版权声明"/>
    </head>
    <body></body>
</html>
```

tips:在实际开发中，一般只会用到keywords和description这两个name属性

##### 2.http-equiv属性

###### tips:在HTML中，meta标签的http-equiv属性只有两个重要作用：定义网页所使用的的编码格式；定义网页自动跳转

```html
<!--定义网页所使用的编码格式-->
<meta charset="utf-8"/>
```

```html
<!--定义网页跳转-->
<meta http-equiv="refresh" content="6;url=https://wwww.baidu.com"/>
<!--表示当前网页会在6秒后，跳转至百度搜索首页-->
```

### 3.2.3 style标签(css)

### 3.2.4 script标签(javascript)

### 3.2.5 link标签(css)

### 3.2.6 base标签（了解即可）

## 3.3 body标签

```html
<!--简单示例-->
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8"/><!--这个代码一定要放在title标签和其他meta标签之前；这是为了放置网页出现乱码-->
        <title>body标签</title>
    </head>
    <body>
        <h3>
            静夜思
        </h3>
        <p>
            窗前明月光，疑是地上霜。
        </p>
        <p>
            举头望明月，低头思故乡。
        </p>
    </body>
```

## 3.4 HTML注释

### 作用：方便理解代码，方便查找

```html
<!--注释的内容-->
```

# unit4: 文本

## 4.1 文本简介
