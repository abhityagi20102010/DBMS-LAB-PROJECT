create table Dept(DEPTNO integer(5),  DNAME varchar(10), LOC varchar(10));
insert into Dept VALUES
(001,"IT","GZB"),(0002,"CSIT","NOIDA"),(003,"CSE","GR.NOIDA"),(004,"CS","DELHI");
ALTER table Dept RENAME TO Department; /*department name change dept to departmentq1 */
ALTER TABLE Department
ADD PINCODE int(6) not null;/*add new column with not null constraint q2*/
/*ALTER TABLE Department DROP column PINCODE
CONSTRAINTS; q3*/
ALTER TABLE Department RENAME COLUMN DNAME TO DEPT_NAME ; /*column name rename command q4*/
ALTER TABLE Department MODIFY LOC CHAR(10) ;/* q5*/
DROP TABLE Department;/*TABLE DELETE*/
SELECT *FROM Department;






create table Employee(EMP_NO integer,EMP_NAME varchar(10),DEPT VARCHAR(10),SALARY int(10),DOJ DATE,BRANCH VARCHAR(10));
insert into Employee values(0001,"RAVI","IT",30000,"2001-01-10","IT-A"),
(0002,"THAKUR","CSIT",30500,"2011-01-10","IT-B"),
(0003,"RAMU","CS",35000,"2011-11-10","IT-C"),
(0004,"AMAN","CSIT",40000,"2015-01-10","IT-A"),
(0005,"RAVIRAJ","CSE",36500,"2020-01-10","IT");
TASK -----
select EMP_NO, SALARY from Employee ;/*EMPNO AND SALARY RETRIVE*/

Select Avg(SALARY) from Employee;/* avg salary find*/
select count(*) from Employee;/*retrive no of emp */
select count(DISTINCT EMP_NAME) FROM Employee; /*q5 */

select EMP_NAME,SUM(SALARY),COUNT(*) FROM Employee  GROUP BY(EMP_NAME); /* Q6 */

SELECT EMP_NAME,SUM(SALARY) FROM Employee GROUP BY(EMP_NAME)
HAVING SUM(SALARY)>12000;/* Q7 */
SELECT EMP_NAME FROM Employee ORDER BY EMP_NAME desc;/* q8*/

SELECT *FROM Employee WHERE EMP_NAME='AMAN' AND SALARY>15000;/*Q9*/

