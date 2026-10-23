# Emp_table.sql
SQL table for employee records, including job title, salary, city, and salary increase.
CREATE TABLE emp (

  empno         NUMBER(4) PRIMARY KEY,

  ename         VARCHAR2(20),

  job          VARCHAR2(20),

  sal          NUMBER(8,2),

  city         VARCHAR2(20),

  increase_percentage  VARCHAR2(10),

  comm         NUMBER(8,2),

  deptno        NUMBER(2),

  hiredate       DATE

);
انشاء جدول EMP
INSERT INTO emp VALUES (1, 'Ahmad', 'MANAGER',  2000, 'Abha',  '10%', NULL, 10, DATE '2020-01-15');

INSERT INTO emp VALUES (2, 'Nasser', 'SECRETARY', 4000, 'Jeddah', '20%', NULL, 20, DATE '2019-03-10');

INSERT INTO emp VALUES (3, 'Ali',  'SALESMAN', 20000, 'Abha',  '10%', 500, 30, DATE '2021-06-01');

INSERT INTO emp VALUES (4, 'Fahad', 'SALESMAN', NULL, 'Najran', '25%', NULL, 30, DATE '2022-11-20');

INSERT INTO emp VALUES (5, 'Saad',  'ANALYST',  3000, 'Abha',  '15%', NULL, 20, DATE '2018-08-08');

INSERT INTO emp VALUES (6, 'Tamer', 'CLERK',   1250, 'Jeddah', '5%', NULL, 10, DATE '2023-02-02');

INSERT INTO emp VALUES (7, 'Majid', 'MANAGER',  5000, 'Riyadh', '10%', NULL, 10, DATE '2017-05-05');
اضافة اعمده وصفوف
SELECT empno, ename, sal FROM emp;
الاستعلام عن ثلاثة اوامر في الجدول
SELECT empno, ename, sal, sal + 500 FROM emp
اضافة عامود افتراضي لعملية الجمع
SELECT empno, ename, sal, sal* 2 FROM emp
اضافة عامود لعملية الضرب
SELECT empno, ename, sal,sal+(sal+40*sal/100)FROM emp;
زيادة الراتب 40%
