## DATABASE:

---

```

create table DEPARTMENT(
     Dno INTEGER NOT NULL,
     Dname VARCHAR(50) DEFAULT NULL,
     Location VARCHAR(50) DEFAULT 'New Delhi',
     PRIMARY KEY(Dno)
);

```

```

create table EMPLOYEE(
     Eno CHAR(3) NOT NULL,
     Ename VARCHAR(50) NOT NULL,
     Job_type VARCHAR(50) NOT NULL,
     Manager CHAR(3) DEFAULT 50,
     Hire_date DATE NOT NULL,
     Dno INTEGER DEFAULT NULL,
     Commission DECIMAL(10,2) DEFAULT 0.0,
     Salary DECIMAL(7,2) NOT NULL,
     PRIMARY KEY(Eno)
);

```
