CREATE DATABASE_name (dhruv); //dhruv is a name

create table_name (info)(  //info is a name
EMP_IDNO int(6),
EMP_FNAME char(50),
EMP_LNAME char(50),
EMP_DEPT int(10)
);

//To insert values into a table.

insert into_name (info) values(127323,'michale','Robbin',57);

//To delete a table.

DROP TABLE_NAME(info); 

// 1 for Colum 
SELECT grade // grade is a colum name.
FROM customer; // customer is a table name.

ALTER TABLE student ADD fee number(10);//add column in orcl 

ALTER TABLE student DROP COLUMN fee;//delete column

ALTER TABLE student MODIFY fee int(10);//data type change

ALTER TABLE student RENAME TO stu;//rename to table name

ALTER TABLE `stu` CHANGE `fee` `RS` INT(10);//change column name in xxamp

ALTER TABLE stu RENAME COLUMN RS TO Fee;// change column name in oracal

INSERT INTO stu VALUES(7890,null,0987654321,8099);//insert into NULL ..

INSERT INTO stu VALUES(7890,'',0987654321,8099);//insert into NULL ..

SELECT * FROM stu;//show table

SELECT * FROM stu WHERE RS is null;//null table show

SELECT * FROM stu WHERE RS is NOT null;//not null table show

SELECT DISTINCT STU_NAME FROM stu;//duplicate value //STU_NAME is name

SELECT * FROM stu WHERE STU_ID=12345 AND STU_NAME='Shreyansh';//aama 1 thay

SELECT * FROM stu WHERE STU_ID=12345 OR STU_NAME='Harpal';// aama 2 thay

SELECT * FROM stu WHERE RS BETWEEN 500 AND 5000;//

SELECT * FROM stu WHERE STU_NAME like 'S%';// only first char 

SELECT * FROM stu WHERE STU_NAME like '%H%';// all name in char 

SELECT * FROM stu WHERE STU_NAME like '_H%';//only second char 


SELECT * FROM stu WHERE STU_NAME like 'H_%';//only first char

SELECT * FROM stu WHERE STU_NAME IN('Harpal','Shreyansh');// only name

UPDATE stu SET STU_NAME='Nandu'WHERE RS=1000;//fild update

SELECT * FROM products WHERE company NOT IN (HP,ASUS,DELL);//othae company in Query

CREATE TABLE st_masterB//
(en_no varchar(12),//
 st_name char(25),//    all primary key
 primary key(en_no));//

ALTER TABLE st_masterb DROP PRIMARY KEY;//primary key delet

ALTER TABLE st_masterb ADD CONSTRAINT st_PK PRIMARY KEY (en_no);// primary key add colum

ALTER TABLE st_masteru ADD CONSTRAINT roll_no UNIQUE (roll_no);//multipal unique

ALTER TABLE st_masteru MODIFY roll_no int NOT NULL;//not null query in table

ALTER TABLE person MODIFY age int NOT null;//convert to null to not null

CREATE TABLE person( ID int PRIMARY KEY, First_name varchar(20)NOT null, Lirst_name varchar(20)NOT null, Age int );//table to primary key

CREATE TABLE person_3( ID int, First_name varchar(20)NOT null, Last_name varchar(20)NOT null, Age int,CONSTRAINT pk_person PRIMARY KEY (First_name,Last_name) );//second way primery key

ALTER TABLE person_3 ADD PRIMARY KEY (ID);//alter throw primary key create

ALTER TABLE person_5 DROP PRIMARY KEY;//drop primary key

SELECT emp.emp_name,dep.dep_name FROM emp INNER JOIN dep on emp.emp_id = dep.emp_id;//used to inner join 

SELECT emp.emp_name,emp.emp_id,dep.dep_name FROM emp LEFT JOIN dep on emp.emp_id = dep.emp_id;//used to left join 

SELECT emp.emp_name,emp.emp_id,dep.dep_name FROM emp RIGHT JOIN dep on emp.emp_id = dep.emp_id;//used to right join 

SELECT * FROM employee_details NATURAL JOIN emp_department; //used to natural join

SELECT * FROM employee_details CROSS JOIN emp_department; //used to cross join

CREATE VIEW abc_view AS SELECT * FROM employee_details NATURAL JOIN emp_department;//used to view
