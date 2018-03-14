# learnSQL

·数据存储三个阶段
人工管理阶段
文件系统阶段
数据库系统阶段

·数据库泛型（数据库规则）也称范式
1nf  2nf 3nf bcnf
第一范式要求表中不能有重复字段，并且每个字段不能再拆分
讲数据库进行进一步细化，细化后变成第二三范式

·DB DBS DBMS
DBS(BD+BDMS+工具)

·sql语言（结构、查询、语言）
三个部分：DDL DML DCL（数据控制语言）

·JDBC是用于执行SQL语句的Java API

·常见数据库系统
甲骨文Oracle
IBM DB2
微软Access 和SQLServer
postgreSQL
MySQL  （Sun）

·SQL语句
CREATE DATABASE 数据库名; 创建
DROP DATABASE 数据库名; 删除
SHOW ENGINES ; 可以查看MySQL数据库支持的存储引擎类型

·存储引擎
InnoDB存储引擎
MyISAM存储引擎
MEMORY存储引擎

·创建表
CREATE TABLE 表名( 
	属性名数据类型[完整性约束条件],
	属性名数据类型[完整性约束条件],
	......
	属性名数据类型
);

·主键
该字段能惟一地标识该表中的每条信息。主键和记录的关系，如同身份证和人的关系。

·外键（关联关系）
	如果字段sno是一个表A的属性，且依赖于表B的主键。那么，称表B为父表，表A为子表，
sno为表A的外键。
	例如，stu_id是student表的主键，stu_id是grade表的外键。当stu_id为‘123’同学
退学了，需要从student表中删除该学生的信息。那么，grade表中stu_id为‘123’的所有信息
也应该同时删除。

·基本查询语句
SELECT 属性列表
FROM 表名和视图列表
[ WHERE 条件表达式1 ]
[ GROUP BY 属性名1 [ HAVING 条件表达式2 ][ WITH ROLLUP ] ]
[ ORDER BY 属性名2 [ ASC | DESC ] ]

例：SELECT num, name, sex,homeaddr FROM employee;

·条件表达式
[ NOT ] IN ( 元素1, 元素2, …, 元素n )
[ NOT ] BETWEEN 取值1 AND 取值2
[ NOT ] LIKE '字符串'
IS [ NOT ] NULL
条件表达式1 AND 条件表达式2 [ … AND 条件表达式n ]
条件表达式1 OR 条件表达式2 [ …OR 条件表达式n ]

·COUNT()函数
SELECT COUNT(*) FROM employee ;
如果要统计employee表中有多少条记

·SUM()函数
使用SUM()函数可以求出表中某个字段取值的总和。如总成绩。

·AVG()函数
使用AVG()函数可以求出表中某个字段取值的平均值。

·MAX()函数

·MIN()函数

·SELECT * FROM info WHERE name REGEXP '^L..y$';
“.”来替代字符串中的任意一个字符

·插入数据
INSERT INTO 表名(属性1, 属性2, … , 属性m) VALUES(值1,值2, …, 值m);
INSERT INTO 表名[ (属性列表) ] VALUES(取值列表1),(取值列表2) … , (取值列表n) ;

·更新数据
UPDATE 表名
SET 属性名1=取值1, 属性名2=取值2,
…,
属性名n=取值n
WHERE 条件表达式;

·删除数据
DELETE FROM 表名[ WHERE 条件表达式] ;

