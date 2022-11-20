# WEB前端课程体系

## MYSQL

### day01

- 关系型数据库逻辑结构

	- 数据库服务器 -> 数据库 -> 数据表 -> 行 -> 列

- 部署结构

	- 服务器端

		- mysqld.exe

	- 客户端

		- mysql.exe

- 客户端连接服务器端

	- mysql.exe   -h127.0.0.1  -P3306  -uroot  -p
	- mysql  -uroot
	- mysql  -uroot<拖拽脚本文件

- 常用的管理命令

	- show  databases;
	- use  数据库名称;
	- show  tables;
	- desc  数据表名称;
	- quit;

- 标准的SQL命令

	- 定义数据结构(DDL)

		- create/drop/alter(修改)

	- 操作数据(DML)

		- insert/delete(删除)/update(修改)

	- 查询数据(DQL)

		- select

	- 控制用户权限(DCL)

		- grant(授权)/revoke(收权)

### day02

- 计算机编码

	- 英文字符

		- ASCII/Latin-1

	- 中文字符

		- GB2312/GBK/Unicode

- MySQL中文乱码产生的原因

	- 默认使用Latin-1编码

- 解决MySQL中文乱码

	- 确保脚本文件编码为utf-8
	- 客户端连接服务器端的编码为utf-8
	- 服务器端创建数据库存储字符的编码为utf-8

- 列类型

	- 数值型

		- tinyint/smallint/int/bigint/float/double/decimal/boolean

	- 日期时间型

		- date/time/datetime

	- 字符串型

		- varchar/char/text

- 列约束

	- 主键约束

		- primary key
		- 自增列

			- auto_increment

	- 非空约束

		- not  null

	- 唯一约束

		- unique

	- 默认值约束

		- 设置默认值

			- default  默认值

		- 使用默认值

	- 检查约束

		- check
		- mysql不支持

	- 外键约束

		- foreign key(外键列)  references  另一个表(主键列)

### day03

- 简单查询

	- 查询特定的列
	- 查询所有的列
	- 给列起别名

		- as

	- 显示不同的记录

		- distinct

	- 查询时执行计算
	- 查询结果排序

		- order  by
		- asc / desc

	- 条件查询

		- where
		- 比较运算符

			- >  <  >=  <=  =  !=

		- and(&&)   /   or(||)
		- is  null/is  not  null
		- in()/not  in()

	- 模糊条件查询

		- %   _ 
		- like

	- 分页查询

		- 两个已知条件

			- 当前的页码
			- 每页的数据量

		- 开始查询的值=(当前的页码-1)*每页的数据量
		- limit  开始查询的值, 每页的数据量
		- 注意：开始查询的值和每页的数据量必须是数值，不能加引号

- 复杂查询

	- 聚合查询/分组查询

		- count()/sum()/avg()/max()/min()
		- group  by
		- year()

	- 子查询
	- 多表查询

		- 内连接

			- inner  join   on

		- 左外连接

			- left   outer  join   on

		- 右外连接

			- right  outer  join   on

		- 全连接

			- mysql不支持
			- 解决方案

				- union
				- union  all

## JS

### day01

- 开发环境

	- 浏览器
	- Node.js

- 变量

	- 声明

		- var  a=1
		- var  b=2,c

	- 命名规则

		- 可以由字母、数字、下划线、美元符号
		- 不能以数字开头
		- 不能使用关键字

	- 赋值

		- 声明变量未赋值则为undefined
		- 允许多次赋值，赋不同类型的值

### day02

- 常量

	- 声明

		- const  pi=3.14

	- 特点

		- 声明后必须赋值
		- 不允许重新赋值

- 数据类型

	- 原始类型

		- 数值型
		- 字符串型
		- 布尔型
		- 未定义型
		- 空

	- 引用类型
	- 检测类型

		- typeof

- 数据类型转换

	- 隐式转换

		- 加号作用

			- 加法运算
			- 字符串拼接

		- 所有隐式转换为数值自动调用函数Number
		- NaN

	- 强制转换

		- Number()/parseInt()/parseFloat()/toString()

- 运算符

	- 算术运算符

		- +  -  *  /   %  ++   --

	- 比较运算符

		- >   <   >=  <=  ==  !=  ===  !==

	- 逻辑运算符

		- &&   ||   !
		- 短路逻辑

	- 位运算符

		- &  |  ^  >>  <<

	- 赋值运算符

		- =   +=   -=   *=    /=...

	- 三目运算符

		- 条件表达式  ?   表达式1  :  表达式2

### day03

- 浏览器端函数

	- alert()/prompt()

- 流程控制

	- if(条件表达式){
   语句块
}
	- if(条件表达式){
   语句块1
}else{
   语句块2
}
	- if(条件表达式1){
   语句块1
}else  if(条件表达式n){
   语句块n
}else{
   语句块n+1
}
	- switch(表达式){
  case  值1:
   语句块1
   break
  case  值n:
   语句块n
   break
  default: 
   语句块n+1
}
	- 转布尔型结果为false

		- 0   NaN  ''   undefined   null

### day04

- 循环

	- while(循环条件){
   循环体
}
	- do{
  循环体
}while(循环条件)
	- for(初始值; 循环条件; 增量){
   循环体
}
	- break

		- 强制结束循环

	- continue

		- 跳过剩余循环体，继续往后执行

	- 循环嵌套

### day05

- 函数

	- 创建

		- function  函数名称(形参列表){
    函数体
    return 值
}

	- 调用

		- 函数名称(实参列表)

- 变量的作用域

	- 全局作用域

		- 全局变量

	- 函数作用域

		- 局部变量

	- 函数中不加var声明的变量是全局变量
	- 程序执行前，会将var声明的变量提升到所在作用域的最前边，只是声明提升，赋值不提升
	- 参数属于是局部变量

### day06

- 函数的作用域

	- 全局函数
	- 局部函数
	- 函数提升
	- 作用域链

- 递归

	- 什么是递归

		- 在函数内调用自身

	- 特点

		- 是一个死循环，用来解决循环问题
		- 容易产生内存泄漏

	- 如何使用

		- 边界条件
		- 找规律
		- 结合return使用

- 匿名函数

	- function(){ }
	- 创建函数

		- var  fun=function(){  }

	- 自调用

		- ;(function(){
    函数作用域
})()

	- 回调函数

		- 把函数作为参数传递
		- tao(  fn  )  /  tao(  function(){} )

- 系统函数

	- isNaN()/eval()

- 对象

	- 分类

		- 自定义对象

			- {  属性名: 属性值,.. }
			- new Object()

		- 内置对象
		- 宿主对象

	- 属性访问

		- 对象.属性名
		- 对象['属性名']

	- 属性遍历

		- for(var k  in  对象){
     k  属性名
    对象[k]   属性值
}

	- 检测属性是否存在

		- 对象.属性名 === undefined
		- 对象.hasOwnProperty('属性名')
		- '属性名'   in  对象

	- 方法

		- var p = {
   name: 'tao',
   run: function(){
       this  指向调用方法的对象
   }
}
p.run()

### day07

- 数据存储

	- 原始类型

		- 存储在栈内存

	- 引用类型

		- 存储在堆内存，会生成一个地址，如果保存到变量中，保存的是地址

	- null

		- 空地址，不指向任何引用类型
		- 可以销毁引用类型

			- var a={} 
a = null

- 数组

	- 创建

		- 字面量

			- [ 元素, 元素... ]

		- 内置构造函数

			- new  Array(元素, 元素...)
			- new  Array(4)

	- 访问

		- 数组[下标]

	- 长度

		- 数组.length
		- 用途

			- 在末尾添加元素

				- 数组[ 数组.length ] = 值

			- 清空数组

				- 数组.length = 0

			- 遍历数组

	- 数组分类

		- 索引数组

			- 以>=0的整数作为下标

		- 关联数组

			- 以字符串作为下标，需要手动添加

	- 遍历数组

		- for(var  k  in  数组){
   k  下标
   数组[k]   元素
}
		- for(var i=0;i<数组.length;i++){
   i  下标
   数组[i]   元素
}

	- API

		- toString()/join()/reverse()/sort()/concat()/slice()/splice()/push()/pop()/unshift()/shift()/indexOf()

	- 二维数组

		- [  [], [], []  ]

### day08

- 字符串对象

	- 包装对象

		- new String()

	- 转为字符串

		- String()

	- 转义字符

		- \

	- API

		- length/charAt()/indexOf()/lastIndexOf()

### day09

- Math对象

	- PI/abs()/pow()/random()/ceil()/floor()/round()/max()/min()

- Date对象

	- 创建

		- new  Date('2022/4/19 9:4:30')
		- new  Date(2022,3,19,9,4,30)
		- new  Date()
		- new  Date(160000000000)

	- 获取

		- getFullYear()/getMonth()/getDate()
		- getHours()/getMinutes()/getSeconds()/getMilliseconds()
		- getDay()
		- getTime()
		- 获取当前时间的时间戳

			- Date.now()

	- 本地字符串

		- toLocaleString()

	- 设置

		- setFullYear()/setMonth()/setDate()
		- setHours()/setMinutes()/setSeconds()/setMilliseconds()
		- setTime()

- Number对象

	- 包装为对象

		- new Number()

	- 转为数值

		- Number()

	- API

		- toFixed()/toString()

- Boolean对象

	- 包装为对象

		- new  Boolean()

	- 转为布尔型

		- Boolean()

	- !!值

		- 隐式转换为布尔型

- 错误处理

	- 常见错误

		- 语法错误
		- 引用错误
		- 类型错误
		- 自定义错误

			- throw  错误内容

	- 错误处理

		- try{
   尝试执行，可能有错误
}catch(err){
   捕获错误，err收集错误信息
   解决错误
}

## NODEJS

### day01

- ES6

	- 块级作用域

		- {   语句块   }
		- let声明变量

			- 变量提升后，暂时无法使用
			- 不允许重复声明

		- 块级作用域下，let和const声明是局部的

	- 参数增强

		- function  fn(a,b,c=0){

}

	- 箭头函数

		- ()=>{    }

	- 模板字符串

		- `字符串 ${JS表达式}`

- 全局对象

	- global

		- 检测是否为全局
		- JS:  window

	- console

		- log()/info()/warn()/error()/time()/timeEnd()

	- process

		- arch/platform/pid/kill()

	- Buffer

		- alloc()  /  toString()

- 模块

	- require()

		- 引入模块，得到模块暴露的对象

	- module

		- 当前模块对象

	- module.exports

		- 当前模块下暴露的对象

	- __dirname

		- 获取当前模块绝对路径

	- __filename

		- 获取当前模块绝对路径+模块名称

### day02

- 模块分类

	- 自定义模块

		- require('./circle.js')

	- 核心模块

		- require('fs')

	- 第三方模块

		- require('mysql')

- 包和npm

	- 包：指第三方模块
	- npm：用来管理包的工具模块
	- npm命令

		- npm   init  -y
		- npm  install  包的名称
		- npm  install

- 网址(URL)

	- http://www.codeboy.com:9999/1.html?kw=手机&a=1
	- new  URL()

- 定时器

	- setTimeout()/clearTimeout()
	- setInterval()/clearInterval()
	- setImmediate()/clearImmediate()
	- process.nextTick()

### day03

- 文件系统模块

	- 引入fs模块
	- stat/writeFile/appendFile/readFile/unlink/copyFile

- 同步和异步

	- 同步

		- 在主程序中执行，会阻止后续代码执行
		- 通过返回值获取结果

	- 异步

		- 在主程序后的事件队列执行，不会阻止主程序后续代码执行
		- 通过回调函数获取结果，通常在回调函数的参数中

- 流(stream)

	- createReadStream()/createWriteStream()
	- 监听事件

		- on('事件名称', 回调函数)

	- pipe()

- http协议

	- 通用头信息

		- 请求的网址
		- 请求的方法
		- 响应的状态码

	- 响应头信息

		- Content-Type
		- Location

	- 请求头信息

- http模块

	- 引入http模块
	- createServer()/listen()
	- 监听请求事件

		- 请求对象

			- req.url/method

		- 响应对象

			- statusCode/write()/setHeader()/end()

### day04

- express模块

	- 下载安装

		- npm   install   express

	- 创建WEB服务器

		- express()/listen()

	- 路由

		- 请求的方法，请求的URL，回调函数
		- 请求对象

			- req.method/url/query/params

		- 响应对象

			- res.send()/redirect()/sendFile()

	- 路由传参

		- get传递

			- 格式

				- http://127.0.0.1:3000/mysearch?a=1&b=2

			- 获取

				- req.query

					- {a:1, b:2}

		- params传递

			- 格式

				- http://127.0.0.1:3000/mysearch/1/2

			- 获取

				- req.params

					- {a:1, b:2}

		- post传递

			- 格式

				- http://127.0.0.1:3000/mysearch

			- 获取

				- 中间件转为对象

					- app.use( express.urlencoded({
   extended: true
}) )

				- req.body

					- {a:1, b:2}

### day05

- 路由器

	- 由一组路由组成，用来管理路由
	- 使用

		- 路由器模块

			- 引入express模块
			- 创建路由器对象

				- express.Router()

			- 添加路由
			- 暴露路由器对象

				- module.exports=对象

		- WEB服务器

			- 引入路由器模块
			- 路由器挂载到WEB服务器

				- app.use( URL, 路由器 )

- 中间件

	- 应用级中间件

		- app.use(  拦截的URL,  函数 )

	- 路由级中间件

		- 路由器的使用

	- 内置中间件

		- 将post传参转对象

			- app.use(express.urlencoded())

		- 托管静态资源

			- app.use( express.static('目录') )

	- 第三方中间件
	- 错误处理中间件

### day06

- mysql模块

	- 下载安装

		- npm  install  mysql

	- 连接

		- 普通连接

			- createConnection()

		- 连接池

			- createPool()

	- 执行SQL命令

		- query(sql命令, [一组要过滤的数据], 回调函数)
		- 占位符(?)

			- 防止SQL注入，先过滤用户传递数据，然后替换占位符

- RESTful接口

	- 请求的URL

		- 版本号、资源名称(复数名词)
		- /v1/users
		- /v1/users/login
		- /v1/emps/2

			- 操作单个资源，使用params传参

	- 请求的方法

		- 增(新建资源)

			- post

				- 使用post传参

		- 删(删除资源)

			- delete

				- 使用params传参

		- 改(修改资源)

			- put

				- 使用post传参

		- 查(获取资源)

			- get

				- 使用params传参

	- 过滤数据

		- 分页过滤

			- /v1/users?pno=1&count=10

		- 使用get传参

	- 返回结果

		- JSON形式

			- 字符串对象

		- '{"code":200, "msg": "登录成功", "data": 一组数据}'

*XMind: ZEN - Trial Version*