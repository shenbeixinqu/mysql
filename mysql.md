## mysql

### 基础查询

#### 1.查询表中的单个字段

```mysql
SELECT last_name FROM employees;
```

#### 2. 查询表中的多个字段

```mysql
SELECT last_name,salary,email FROM employees;
```

#### 3.查询表中的所有字段

```mysql
SELECT * FROM employees;
```

#### 4.查询常量值

```mysql
SELECT 100;
SELECT 'john';
```

#### 5.查询表达式

```mysql
SELECT 100%98;
```

#### 6.查询函数

```mysql
 SELECT VERSION();
```

#### 7.起别名

```mysql
#方式一：使用as
SELECT 100%98 AS 结果;
SELECT last_name AS 姓,first_name AS 名 FROM employees;

#方式二：使用空格
SELECT last_name 姓,first_name 名 FROM employees;

#案例：查询salary，显示结果为 out put
SELECT salary AS "out put" FROM employees;
```

#### 8.去重

```mysql
#案例：查询员工表中涉及到的所有的部门编号
SELECT DISTINCT department_id FROM employees;
```

#### 9.+号的作用

```mysql
#案例：查询员工名和姓连接成一个字段，并显示为 姓名

SELECT CONCAT('a','b','c') AS 结果;

SELECT 
	CONCAT(last_name,first_name) AS 姓名
FROM
	employees;
```

### 条件查询

#### 1.按条件表达式筛选

```mysql
#案例1：查询工资>12000的员工信息
SELECT 
	*
FROM
	employees
WHERE
	salary>12000;

#案例2：查询部门编号不等于90号的员工名和部门编号
SELECT 
	last_name,
	department_id
FROM
	employees
WHERE
	department_id<>90;
```

#### 2.按逻辑表达式筛选

```mysql
#案例1：查询工资z在10000到20000之间的员工名、工资以及奖金
SELECT
	last_name,
	salary,
	commission_pct
FROM
	employees
WHERE
	salary>=10000 AND salary<=20000;
#案例2：查询部门编号不是在90到110之间，或者工资高于15000的员工信息
SELECT
	*
FROM
	employees
WHERE
	NOT(department_id>=90 AND  department_id<=110) OR salary>15000;
```

#### 3.模糊查询

##### like

```mysql
#案例1：查询员工名中包含字符a的员工信息
select 
	*
from
	employees
where
	last_name like '%a%';#abc
#案例2：查询员工名中第三个字符为e，第五个字符为a的员工名和工资
select
	last_name,
	salary
FROM
	employees
WHERE
	last_name LIKE '__n_l%';
#案例3：查询员工名中第二个字符为_的员工名

SELECT
	last_name
FROM
	employees
WHERE
	last_name LIKE '_$_%' ESCAPE '$';(escape作用为转义)
```

##### between and

```mysql
#案例1：查询员工编号在100到120之间的员工信息
SELECT
	*
FROM
	employees
WHERE
	employee_id BETWEEN 120 AND 100;
```

##### in

```mysql
特点：
	①使用in提高语句简洁度
	②in列表的值类型必须一致或兼容
	③in列表中不支持通配符
#案例：查询员工的工种编号是 IT_PROG、AD_VP、AD_PRES中的一个员工名和工种编号
SELECT
	last_name,
	job_id
FROM
	employees
WHERE
	job_id IN( 'IT_PROT' ,'AD_VP','AD_PRES');
```

##### is null

```mysql
#案例1：查询没有奖金的员工名和奖金率
SELECT
	last_name,
	commission_pct
FROM
	employees
WHERE
	commission_pct IS NULL;


#案例1：查询有奖金的员工名和奖金率
SELECT
	last_name,
	commission_pct
FROM
	employees
WHERE
	commission_pct IS NOT NULL;
```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

#### 

```mysql

```

