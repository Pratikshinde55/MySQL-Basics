# MySQL-Basics

## DBMS(Data Base Management System)
There are Two types of DBMS: 
1. SQL (RDBMS-Relational DataBase Management System)
2. NoSQL

In SQL & NoSQL Classifiaction:

| SQL-RDBMS | NoSQL |
| ----------- | ----------- |
| MySQL | MongoDB |
| MariaDB | Casendra |
| MsSQL | HBase |
| DB2 |     |
| PostgreQL |    |
| Oracle |   |

Storing data in Hard Disk is permanent/persistant data.

For Storing Data in HD that must be in "file".

### MySQL & MariaDB Port NO:- 3306

### Table & Data Base:
DataBase is just concept behind the scence the "data" is arranged in specific model, that data is put in "file" that is known as "Table".
& That file is always put in Directory/Folder that directory is known as "Data Base".

## Installation of MySQL on Window:

MySQL Community Download MSI Installer link : [MySOL-MSI_installer-link](https://dev.mysql.com/downloads/installer/)

- Click On Custom
![MySQL-custom](https://github.com/user-attachments/assets/9dacd1c8-da72-456b-a368-b276a7babaa2)

- Select MySQL Server & Workbench
![MySQL-server](https://github.com/user-attachments/assets/40dc400e-f67e-400c-9d3d-167997ba1984)

- Then click next, execute then next
![MySQL-insatll](https://github.com/user-attachments/assets/fe991d93-288d-489a-b6ad-200f8628defa)

- Strong Password for version 8
![MySQL-Pass](https://github.com/user-attachments/assets/b36e80ce-85d3-4669-98e7-ad542ec3880a)

- Create Password for MySQL, To access MySQL we need to connect MySQL Server for this we use Authentication:(MySQL root user have unlimited power)
![MySQL-Set-pass](https://github.com/user-attachments/assets/ae704f67-4bab-479f-81c8-fb05c3b2d749)

- Start Workbench 
![MySQL-set](https://github.com/user-attachments/assets/2d4a13e5-02a7-4cc5-aa72-998a5002f3f6)

- MySQL Workbench open
![MySQL-Workbench](https://github.com/user-attachments/assets/052d7a48-dc2d-4ee9-b57c-797f7bd26b4d)

- Go to "+" button to add new user 'MySQL Connection' then fill info, then Test connection and fill password that was created during Installation:
![MySQL-Add-pratik-connection](https://github.com/user-attachments/assets/25429486-122b-46e8-9254-4fa49c82021e)

- Here see pratik user created and click on that we land on Client Workbench:
![Land-workbench](https://github.com/user-attachments/assets/47fc95f0-9a99-4610-9abd-a8bc0e7c4631)

## On Workbech:
on "MySQL WorkBench" can run query from created connection.

- Note:
1. There is no special need of remember or maintain Capital or Small letters syntax in MySQL.
2. In MySQL for string data type use "char" or "varchar".
3. We can put data in table, that data if is string & char then we put that data in "..." or '...'.


**To Check List of Data Base Query is:**

    show databases;

**To Check list of Tables query is:**

    show tables;

**Create Data Base query:**

    create database psDB;

**To Use Data Base then query is:**

    use psDB;

**Create Table in Data Base:**

    create table Students(YearOfPass int, nameSTD char(30), mobile char(10), remark char(7) );
    
![create-table](https://github.com/user-attachments/assets/ad45c439-9eaf-4d0b-8227-cf1e94d9a5e6)

**Describe Table query:**

    describe table Students;

### Insert data into table: [Insert into table-name values()]
There are different approch to add data in table:

1. Just add data in series:

       insert into Students values(24, "Pratik Shinde", 1234567890, 'nice');

2. Add Specific values in certain coloumn:

        insert into Students (nameSTD, remark) values("Luckhan", 'pass');

3. Add Values:

        insert into students (YearOfPass, nameSTD, mobile, remark) values(2024, "Soma", 1234123412, 'pass');

4. Add multiple values in Table in single query:

        insert into students (YearOfPass, nameSTD, mobile, remark) values(2020, "Panakj", 0535, 'good'), (20222, "Datta", 96171819, 'ok'), (2018, "Sagar", 11111111, 'fail');

![insert-query](https://github.com/user-attachments/assets/bd21bb91-553b-4ed3-a98b-af38d7af0737)


### To Read Data query or Retrieve:
There different way to retrieve data

1. To retrieve data:

        select * from Students;

2. To retrieve specific column:

        select  nameSTD, remark from Students;

![select-1](https://github.com/user-attachments/assets/371149c4-134d-492b-97bd-1c23bf993447)

3. To retrieve specific values in column:

        select * from Students where nameSTD="Pratik Shinde" ;

![select-2](https://github.com/user-attachments/assets/1f7011bf-c3e4-4524-bd11-8448e37d2098)
  
4. To retrieve specific coloumn with specific values:

        select mobile from Students where nameSTD="Sagar" ;

![select-3](https://github.com/user-attachments/assets/a49e5fa6-3129-402a-aa29-ddce1d22773e)

5. select sum() function:

         select sum(mobile) from Students where nameSTD='Pratik Shinde'

6. count ():

         select count() from Students;


## Normalization: [Data Base design:- Normalization & RDBMS]
Normalization is a efficent way to organize data in the Data Base.

**unique:** To avoid duplication in table data we use "unique" keyword.

**auto_increment:** This keyword we use during create a table, This helps to automatic increment in number & make specific column.

**enum:** enum data type/keyword used in MySQL to fix table certain values. 

**char:** We use char for phone no. because phone no. is 10 digit When we use int then is problem in memory allocation.

**decimal:** price decimal(3, 2), If any value in decimal then we use decimal keyword in query during creating table.


       create table Students (
	 StudentID int unique auto_increment,
         name char(30),
         Gender  enum("Male" , "Female"),
         Phone  char(12),
         Course char(40),
         CoursePrice  decimal(3,2),
         RegTime char(20),
         Teacher char(15)
       );

Insert values in table:

    INSERT INTO Students(
    name, Gender, Phone, CoursePrice, RegTime, Course, Teacher
    )
    VALUES
    ('Pratik Shinde', 'Male', 98505555, 3.5, '2023-01-30', 'DevOps', 'Vimal'),
    ('Pankaj', 'Male', 11105350, 1.2, '2022-02-03', 'MachineLearning', 'Patil'),
    ('Soma', 'Male', 12341234, 1.5, '2024-09-15', 'AI', 'Vimal'),
    ('Lucky', 'Male', 111112222, 2.2, '2024-12-29', 'Application', 'Kande'),
    ('Shrdha', 'Female', 123123123, 3.5, '2018-10-22', 'DevOps', 'Vimal');
    
![Normalization-table](https://github.com/user-attachments/assets/bacd0567-2bfd-4386-a8fc-1b8fff3c4061)

- Schemas:- "Schemas is Virtual planning or all data. Schemas also known as DataBase. Schemas show all sturcture of tables, columns DataBase."
- Primary Key:- "Primary key serve as unique identifiers for each row in database table."
- **Foreign key:-** "Foreign key link data in one table to the data in another table." 
