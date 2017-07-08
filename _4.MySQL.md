# 数据库SQL操作

# 什么是SQL语句

SQL是一门ANSI的标准计算机语言，用来访问和操作数据库系统。SQL语句用于取回和更新数据库中的数据。SQL可与数据库程序协同工作，比如MS Access、DB2、Informix、MS SQL Server、Oracle、Sybase以及其他数据库系统。

说明：

* SQL指结构化查询语句

* SQL使我们有能力访问数据库

* SQL是一种ANSI的标准计算机语言

不幸地是，存在着很多不同版本的 SQL 语言，但是为了与 ANSI 标准相兼容，它们必须以相似的方式共同地来支持一些主要的关键词（比如 SELECT、UPDATE、DELETE、INSERT、WHERE 等等）。

# SQL能做什么

* SQL 面向数据库执行查询

* SQL 可从数据库取回数据

* SQL 可在数据库中插入新的记录

* SQL 可更新数据库中的数据

* SQL 可从数据库删除记录

* SQL 可创建新数据库

* SQL 可在数据库中创建新表

# RDBMS关系型数据库管理系统

RDBMS 指的是关系型数据库管理系统。

RDBMS 是 SQL 的基础，同样也是所有现代数据库系统的基础，比如 MS SQL Server, IBM DB2, Oracle, MySQL 以及 Microsoft Access。

RDBMS 中的数据存储在被称为表（tables）的数据库对象中。

表是相关的数据项的集合，它由列和行组成。

# SQL DML 和 DDL

可以把 SQL 分为两个部分：数据操作语言 (DML) 和 数据定义语言 (DDL)。

SQL (结构化查询语言)是用于执行查询的语法。但是 SQL 语言也包含用于更新、插入和删除记录的语法。

**查询和更新指令构成了 SQL 的 DML 部分：** 

* SELECT - 从数据库表中获取数据

* UPDATE - 更新数据库表中的数据

* DELETE - 从数据库表中删除数据

* INSERT INTO - 向数据库表中插入数据

SQL 的数据定义语言 (DDL) 部分使我们有能力创建或删除表格。我们也可以定义索引（键），规定表之间的链接，以及施加表间的约束。

**SQL 中最重要的 DDL 语句:**

* CREATE DATABASE - 创建新数据库

* ALTER DATABASE - 修改数据库

* CREATE TABLE - 创建新表

* ALTER TABLE - 变更（改变）数据库表

* DROP TABLE - 删除表

* CREATE INDEX - 创建索引（搜索键）

* DROP INDEX - 删除索引

# 常用SQL语句实现

本课程将使用navicat软件对数据库进行操作。我们需要连接上我们本机的数据库。并选中world数据库中的city表格进行操作。

[参考网址](http://www.w3school.com.cn/sql/index.asp)

## 1. SELECT语句

SELECT 语句用于从表中选取数据。结果被存储在一个结果表中（称为结果集）。

**语法格式**

```SQL
SELECT 列名称 FROM 表名称;
SELECT * FROM 表名称;
```

注释：SQL 语句对大小写不敏感。SELECT 等效于 select。

**[SELECT案例一]**

如需获取名为 “LastName” 和 “FirstName” 的列的内容（从名为 “Persons” 的数据库表），请使用类似这样的 SELECT 语句：

```SQL
SELECT LastName , FirstName From persons;
```
"persons"表：

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%935%E6%95%B0%E6%8D%AE%E5%BA%93SQL%E6%93%8D%E4%BD%9C/images/20161209144430.jpg)

查询结果：

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%935%E6%95%B0%E6%8D%AE%E5%BA%93SQL%E6%93%8D%E4%BD%9C/images/20161209144642.jpg)

**[SELECT案例二]**

现在我们希望从 “Persons” 表中选取所有的列。

请使用符号 * 取代列的名称，就像这样：

```SQL
SELECT * FROM Persons
```
提示：星号是选取所有列的快捷方式。

结果：

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%935%E6%95%B0%E6%8D%AE%E5%BA%93SQL%E6%93%8D%E4%BD%9C/images/20161209144709.jpg)

## 2. WHERE 语句

如需有条件地从表中选取数据，可将 WHERE 子句添加到 SELECT 语句。

```SQL
SELECT 列名称 FROM 表名称 WHERE 列 运算符 值
```

如果只希望选取居住在城市 “Beijing” 中的人，我们需要向 SELECT 语句添加 WHERE 子句：

```SQL
SELECT * FROM Persons WHERE City='Beijing'
```

"persons"表

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%935%E6%95%B0%E6%8D%AE%E5%BA%93SQL%E6%93%8D%E4%BD%9C/images/20161209144000.jpg)

结果：

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%935%E6%95%B0%E6%8D%AE%E5%BA%93SQL%E6%93%8D%E4%BD%9C/images/20161209144256.jpg)

## 3. INSERT INTO 语句

INSERT INTO 语句用于向表格中插入新的行。

**语法格式**

```SQL
INSERT INTO 表名称 VALUES (值1, 值2,....)
```

我们也可以指定所要插入数据的列：

```SQL
INSERT INTO table_name (列1, 列2,...) VALUES (值1, 值2,....)
```

**【插入案例1】**

“Persons” 表：

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%935%E6%95%B0%E6%8D%AE%E5%BA%93SQL%E6%93%8D%E4%BD%9C/images/20161209144752.jpg)

SQL语句：

```SQL
INSERT INTO Persons VALUES ('Gates', 'Bill', 'Xuanwumen 10', 'Beijing');
```

结果

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%935%E6%95%B0%E6%8D%AE%E5%BA%93SQL%E6%93%8D%E4%BD%9C/images/20161209144818.jpg)

**【插入案例2】**

在指定的列中插入数据

“Persons” 表：

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%935%E6%95%B0%E6%8D%AE%E5%BA%93SQL%E6%93%8D%E4%BD%9C/images/20161209144844.jpg)

SQL语句：

```SQL
INSERT INTO Persons (LastName, Address) VALUES ('Wilson', 'Champs-Elysees')
```

结果：

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%935%E6%95%B0%E6%8D%AE%E5%BA%93SQL%E6%93%8D%E4%BD%9C/images/20161209144859.jpg)

## 4. UPDATE

Update 语句用于修改表中的数据。

**语法结构：**

```SQL
UPDATE 表名称 SET 列名称 = 新值 WHERE 列名称 = 某值
```

person表

![](4.UPDATE

Update 语句用于修改表中的数据。

语法：

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%935%E6%95%B0%E6%8D%AE%E5%BA%93SQL%E6%93%8D%E4%BD%9C/images/20161209145745.jpg)

**【更新案例1】**

更新某一行中的一个列

我们为 lastname 是 “Wilson” 的人添加 firstname：

```SQL
UPDATE Person SET FirstName = 'Fred' WHERE LastName = 'Wilson';
```

结果：

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%935%E6%95%B0%E6%8D%AE%E5%BA%93SQL%E6%93%8D%E4%BD%9C/images/20161209145843.jpg)

**【更新案例2】**

更新某一行中的若干列

我们会修改地址（address），并添加城市名称（city）：

```SQL
UPDATE Person SET Address = 'Zhongshan 23', City = 'Nanjing'
WHERE LastName = 'Wilson;
```

结果：

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%935%E6%95%B0%E6%8D%AE%E5%BA%93SQL%E6%93%8D%E4%BD%9C/images/20161209150001.jpg)

## 4. DELETE 语句

DELETE 语句用于删除表中的行。

**语法格式:**
```SQL
DELETE FROM 表名称 WHERE 列名称 = 值
```

Person表

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%935%E6%95%B0%E6%8D%AE%E5%BA%93SQL%E6%93%8D%E4%BD%9C/images/20161209150220.jpg)

**【删除案例1】**

删除某行

“Fred Wilson” 会被删除：

```SQL
DELETE FROM Person WHERE LastName = 'Wilson'
```

结果:

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%935%E6%95%B0%E6%8D%AE%E5%BA%93SQL%E6%93%8D%E4%BD%9C/images/20161209150338.jpg)

删除所有行

可以在不删除表的情况下删除所有的行。这意味着表的结构、属性和索引都是完整的：

```SQL
DELETE FROM table_name
```

或者：

```SQL
DELETE * FROM table_name
```

