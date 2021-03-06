# 什么是数据库

简单的说， 数据库（databese）就是一个存放数据的仓库，这个仓库是按照一定的数据结构（数据结构是指数据的组织形式或数据之间的联系）来组织。存储的，我们可以通过数据提供的多种方法来管理数据库里的数据。

# 常见的数据库

数据库通常分为层次式数据库、网络式数据库和关系式数据库三种。而不同的数据库是按不同的数据结构来联系和组织的。而在当今的互联网中，最常见的数据库模型主要是两种，即_关系型数据库_和_费关系型数据库_。

# 关系型数据库

关系型数据库模型是把复杂的数据结构归结为简单点的二元关系（即二维表格形式）。在关系型数据库中，对数据的操作几乎全部建立在一个或多个关系表格上，通过对这些关联的表格分类、合并、链接或选取等运算来实现数据库的管理。

关系型数据库诞生40多年了， 从理论产生发展到现实产品，例如：Qracle和MySQL，Qracle在数据库领域上升到霸主地位

# 非关系型的数据库

NoSQL,泛指非关系型的数据库。随着互联网web2.0网站的兴起，传统的关系型数据库在应付web2.0网站，特别是超大规模和高并发的SNS类型的web2.0纯动态网站已经显得力不从心，暴露了很多难以克服的问题，而非关系型的数据库则由于其本身的特点得到了非常迅速的发展。NoSQL数据库在特定的场景下可以发挥出难以想象的高效率和高性能，它是作为对传统关系型数据库的一个有效补充。

NoSQL（= Not Only SQL），意即“不仅仅是SQL”，是一项全新的数据库革命性运动，早期就有人提出，发展至2009年去世越发高涨。NoSQL的拥护者们提倡运用非关系型的数据库，相对于铺天盖地的关系型数据库的运用，这一概念无疑是一种全新的思维的注入。

# 常用关系型数据库产品介绍

## Oracle数据库

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%931%E6%95%B0%E6%8D%AE%E5%BA%93%E7%AE%80%E4%BB%8B/images/20170116123725.jpg)

Oracle数据库系统是美国ORCALE公司（甲骨文）提供的以分布式数据库为核心的一组软件产品，是目前最流行的客户/服务器（CLIENT/SERVER）或者B/S体系结构的数据库之一。比如SliverStream就是基于数据库的一种中间件。Oracle数据库是目前世界上使用最为管饭的数据库管理系统。作为一个通用的数据库系统，它具有完整的数据管理功能；作为一个关系数据库，它是一个完备关系的产品；作为分布式数据库他实现了分布式处理功能。而且，只要在一种机型上学习了Oracle知识，便能在各种类型的机器上使用它

Oracle数据库最新版本为Oracle datebase 12c。Oracle数据库12c 引入了一个新的多承租方架构，使用该架构可轻松部署和管理数据库云。此外，一些创新特性可最大限度地提高资源使用率和灵活性，如Oracle Multitenant可快速整合多个数据库，而Automatic Data Optimization和Heat Map能以更高的密度压缩数据和对数据分层。这些独一无二的技术进步再加上在可用性、安全性和大数据支持方面的主要增强，使得Oracle数据库12c 成为私有云和公有云部署的理想平台。

## MySQL数据库

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%931%E6%95%B0%E6%8D%AE%E5%BA%93%E7%AE%80%E4%BB%8B/images/20170116103339.jpg)

MySQL（发音为“my ess cue el”，不是“my sequel”）是一种开放源代码的关系型数据库管理系统（RDBMS），MySQL数据库系统使用最常用的数据库管理语言–结构化查询语言（SQL）进行数据库管理。
 
由于MySQL是开放源代码的，因此任何人都可以在General Public License的许可下下载并根据个性化的需要对其进行修改。MySQL因为其速度、可靠性和适应性而备受关注。大多数人都认为在不需要事务化处理的情况下，MySQL是管理内容最好的选择。
  
MySQL这个名字，起源不是很明确。一个比较有影响的说法是，基本指南和大量的库和工具带有前缀“my”已经有10年以上，而且不管怎样，MySQL AB创始人之一的Monty Widenius的女儿也叫My。这两个到底是哪一个给出了MySQL这个名字至今依然是个迷，包括开发者在内也不知道。
   
## MariaDB数据库

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%931%E6%95%B0%E6%8D%AE%E5%BA%93%E7%AE%80%E4%BB%8B/images/20170116103757.jpg)

MariaDB数据库管理系统是MySQL的一个分支，主要由开源社区在维护，采用GPL授权许可。开发这个分支的原因之一是：甲骨文公司收购了MySQL后，有将MySQL闭源的潜在风险，因此社区采用分支的方式来避开这个风险。 MariaDB的目的是完全兼容MySQL，包括API和命令行，使之能轻松成为MySQL的代替品。在存储引擎方面，使用XtraDB（英语：XtraDB）来代替MySQL的InnoDB。 MariaDB由MySQL的创始人Michael Widenius（英语：Michael Widenius）主导开发，他早前曾以10亿美元的价格，将自己创建的公司MySQL AB卖给了SUN，此后，随着SUN被甲骨文收购，MySQL的所有权也落入Oracle的手中。MariaDB名称来自Michael Widenius的女儿Maria的名字。
  
## SqlServer数据库

![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%931%E6%95%B0%E6%8D%AE%E5%BA%93%E7%AE%80%E4%BB%8B/images/20170116104019.jpg)

SQL Server是由Microsoft开发和推广的关系数据库管理系统（DBMS），它最初是由Microsoft、Sybase和Ashton-Tate三家公司共同开发的，并于1988年推出了第一个OS/2版本。Microsoft SQL Server近年来不断更新版本，1996年，Microsoft 推出了SQL Server 6.5版本；1998年，SQL Server 7.0版本和用户见面；SQL Server 2000是Microsoft公司于2000年推出，目前最新版本是2012年3月份推出的SQL SERVER 2012。
 
## Access数据库
 
![](https://nts.newbieol.com/static/k25/03_%E5%BC%95%E6%93%8E%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6/%E5%8D%8F%E5%90%8C%E5%BC%80%E5%8F%91%E4%B8%8E%E6%95%B0%E6%8D%AE%E5%BA%93%E5%9F%BA%E7%A1%80/%E6%95%B0%E6%8D%AE%E5%BA%93/%E6%95%B0%E6%8D%AE%E5%BA%931%E6%95%B0%E6%8D%AE%E5%BA%93%E7%AE%80%E4%BB%8B/images/20170116104131.jpg)
 
Microsoft Office Access是微软把数据库引擎的图形用户界面和软件开发工具结合在一起的一个数据库管理系统。它是微软OFFICE的一个成员, 在包括专业版和更高版本的office版本里面被单独出售。2012年12月4日,最新的微软Office Access 2013在微软Office 2013里发布,微软Office Access 2010 是前一个版本。
 
MS ACCESS以它自己的格式将数据存储在基于Access Jet的数据库引擎里。它还可以直接导入或者链接数据(这些数据存储在其他应用程序和数据库)。
 
软件开发人员和数据架构师可以使用Microsoft Access开发应用软件,“高级用户”可以使用它来构建软件应用程序。和其他办公应用程序一样，ACCESS支持Visual Basic宏语言,它是一个面向对象的编程语言,可以引用各种对象，包括DAO(数据访问对象),ActiveX数据对象,以及许多其他的ActiveX组件。可视对象用于显示表和报表，他们的方法和属性是在VBA编程环境下，VBA代码模块可以声明和调用Windows操作系统函数。
  
  
