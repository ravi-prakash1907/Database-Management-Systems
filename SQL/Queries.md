#SYLLABUS QUERIES:


```

1)      SELECT
        Eno, Ename, Job_type, Hire_date
        FROM EMPLOYEE;

```
```

2)      SELECT
        DISTINCT Job_type
        FROM EMPLOYEE;

```
```

3)      SELECT
        CONCAT(Ename, ',', Job_type)
        FROM EMPLOYEE;

```
```

4)      SELECT
        CONCAT(Eno, ', ', Ename, ', ', Job_type, ', ', Manager, ', ', Hire_date, ', ', Dno, ', ', Commission, ', ', Salary)
        AS THE_OUTPUT
        FROM EMPLOYEE;

```
```

5)      SELECT
        Ename, Salary
        FROM EMPLOYEE
        WHERE Salary > 2850;

```
```

6)      SELECT
        Ename, Dno
        FROM EMPLOYEE
        WHERE Eno = '7900';

```
```

7)      SELECT
        Ename, Salary
        FROM EMPLOYEE
        WHERE Salary NOT BETWEEN 1500 AND 2850;

```
```

8)      SELECT
        Ename, Dno
        FROM EMPLOYEE
        WHERE Dno IN (1, 3)
        ORDER BY Ename ASC;

```
```

9)      SELECT
        Ename, Hire_date
        FORM EMPLOYEE
        WHERE YEAR(Hire_date) = '2018';

```
```

10)     SELECT
        Ename, Job_type
        FROM EMPLOYEE
        WHERE Manager = NULL;

```
```

11)     SELECT
        Ename, Salary, Commission
        FROM EMPLOYEE
        WHERE Commission IS NOT NULL;

```
```

12)     SELECT
        *
        FROM EMPLOYEE
        ORDER BY Commission DESC;     /  Salary DESC;

```
```

13)     SELECT
        Ename
        FROM EMPLOYEE
        WHERE Ename LIKE '__A%';

```
```

14)     SELECT
        Ename
        FROM EMPLOYEE
        WHERE (Ename LIKE '%R%R%' OR '%A%A%') AND (Dno = 30 OR Manager = '7788');

```
```

15)     SELECT
        Ename, Salary, Commission
        FROM EMPLOYEE
        WHERE Commission = 14+(Salary + (0.05*Salary));

```
```

16)     SELECT CURDATE();

```
```

17)     < NOT YET DONE >

```
```

18)     SELECT
        Ename, CEIL(DATEDIFF(CURDATE(), HIRE_DATE)/30) AS 'NUMBER OF MONTHS'
        FROM EMPLOYEE;

```
```

19)     SELECT
        CONCAT(Ename, ' earns ', Salary, ' monthly but wants ', 3*Salary) AS 'DREAM SALARY'
        FROM EMPLOYEE;

```
```

20)     SELECT CONCAT(UCASE(LEFT(Ename, 1)), LCASE(RIGHT(Ename, CHAR_LENGTH(Ename)-1))) AS Ename FROM EMPLOYEE WHERE Ename LIKE 'J%' OR 'A%' OR 'M%';

```
```

21)     SELECT ename, hire_date, dayname(hire_date) as 'DAY OF WEEK' FROM EMPLOYEE;

```
```

22)     SELECT Ename, Dname, EMPLOYEE.Dno from EMPLOYEE join DEPARTMENT on EMPLOYEE.Dno=DEPARTMENT.Dno;

```
```

23)     SELECT DISTINCT Job_type FROM EMPLOYEE WHERE Dno = '#30';

```
```

24)     SELECT Ename, Dname FROM EMPLOYEE JOIN DEPARTMENT ON EMPLOYEE.Dno=DEPARTMENT.Dno WHERE Ename LIKE '%A%';

```
```

25)    SELECT Ename, Job_type, EMPLOYEE.Dno, Dname FROM EMPLOYEE JOIN DEPARTMENT ON EMPLOYEE.Dno=DEPARTMENT.Dno WHERE Location='Dallas';     

```
```

26)     SELECT E.Eno, E.Ename, M.Eno as 'Manager Enum', M.Ename as 'Manager Ename' FROM EMPLOYEE AS E, EMPLOYEE AS M where E.Manager= M.Eno union select Eno, Ename, NULL, NULL from EMPLOYEE where Manager is NULL;

```
```

27)     SELECT Ename, Dno, Salary FROM EMPLOYEE WHERE (Dno, Salary) IN (SELECT Dno, Salary FROM EMPLOYEE WHERE Commission > 0.00);

```
```

28)     SELECT Ename, RPAD("*",ceil(Salary/100),'*') as 'Salary' from EMPLOYEE;

```
```

29)     SELECT MAX(Salary) AS 'HIGHEST', MIN(Salary) AS 'LOWEST', SUM(Salary) AS 'SUM', AVG(Salary) AS 'AVERAGE' FROM EMPLOYEE;

```
```

30)     SELECT COUNT(*) AS 'No of Employees' FROM EMPLOYEE GROUP BY Job_type;

```
```

31)     SELECT COUNT(DISTINCT(Manager)) FROM EMPLOYEE;

```
```

32)     SELECT Dname,Location, COUNT(*) AS 'No of Employees', AVG(SALARY) FROM DEPARTMENT AS D JOIN EMPLOYEE AS E ON D.Dno=E.Dno GROUP BY D.Dno;

```
```

33)     SELECT Ename, Hire_date FROM EMPLOYEE AS E join DEPARTMENT AS D ON E.Dno = D.Dno WHERE E.Dno = (SELECT Dno FROM EMPLOYEE WHERE Ename = 'Blake');

```
```

34)     SELECT Eno, Ename FROM EMPLOYEE WHERE Salary > (SELECT AVG(Salary));

```
```

35)     SELECT Eno, Ename FROM EMPLOYEE AS E join DEPARTMENT AS D ON E.Dno = D.Dno WHERE Dname LIKE '%T%';

```
```

36)     SELECT E.Dno, Ename, Job_type FROM EMPLOYEE AS E join DEPARTMENT AS D ON E.Dno = D.Dno WHERE Dname = 'Sales';

```
```

37)     SELECT E.Dno, Ename, Job_type FROM EMPLOYEE AS E join DEPARTMENT AS D ON E.Dno = D.Dno WHERE Location = 'New Delhi';

```
```


-------------------------------------------------
