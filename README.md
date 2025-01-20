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
1. There is no special need of remember or maintain capital small letter syntax in MySQL.
2. We can use ; & If we don't use ; then also query run.
3. We can put data in table, that data if is string & char then we put that data in "..." or '...'.


To Check List of Data Base Query is:

    show databases;

To Check list of Tables query is:

    show tables;

Create Data Base query:

    create database psDB;

To Use Data Base then query is:

    use psDB;

Create Table in Data Base:

    create table Students(YearOfPass int, name char, mobile int, remark char(7) );
