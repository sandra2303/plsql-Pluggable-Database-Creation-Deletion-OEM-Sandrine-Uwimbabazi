# plsql-Pluggable-Database-Creation-Deletion-OEM-Sandrine-Uwimbabazi
PDB
# 🧩 Assignment 2: Database Creation, Deletion & OEM

### Student: Uwimbabazi Sandrine  
### Student ID: 27399  
### Course: Database Development with PL/SQL 
### Instructor: Eric Maniraguha  
### Date: 8 October 2025  

---

## 🪄 Introduction

This project demonstrates how to create, manage, and delete Oracle Pluggable Databases (PDBs) in *Oracle Database 21c XE, and how to use **Oracle Enterprise Manager (OEM)* for monitoring.
.  

The assignment is divided into three main tasks:
1. Creating a new PDB.  
2. Deleting an existing PDB.  
3. Monitoring databases using OEM.  

Through these tasks, the student demonstrates hands-on skills in **database creation, management, and monitoring** within Oracle’s multitenant environment.

---


### 🧠 Task 1 – Create a New Pluggable Database

#### Objective  
To create a new pluggable database named `sa_pdb_27399` from the seed PDB.

#### SQL Code
```sql


 CREATE PLUGGABLE DATABASE sa_pdb_27399
    ADMIN USER Sandrine_plsqlauca_27399 IDENTIFIED BY sandra123
    FILE_NAME_CONVERT = (
    'C:\APP\ADMINISTRATOR\PRODUCT\21C\ORADATA\XE\PDBSEED\',
    'C:\APP\ADMINISTRATOR\PRODUCT\21C\ORADATA\XE\SA_PDB_27399\'
    );
```
![create PDB](https://github.com/sandra2303/plsql-Pluggable-Database-Creation-Deletion-OEM-Sandrine-Uwimbabazi/blob/main/screenshots/create%20pdb.PNG)

---

```sql

ALTER PLUGGABLE DATABASE sa_pdb_27399 OPEN;
```
![alter open](https://github.com/sandra2303/plsql-Pluggable-Database-Creation-Deletion-OEM-Sandrine-Uwimbabazi/blob/main/screenshots/alter%20open.PNG)

---

### 🧱 Task 2: Create and Delete Another PDB

#### Objective

To create, close and delete the PDB named sa_to_delete_pdb_27399.

#### To create

#### SQL Code
```sql


 CREATE PLUGGABLE DATABASE sa_to_delete_pdb_27399
    ADMIN USER Sandrine_plsqlauca_27399 IDENTIFIED BY sandra123
    FILE_NAME_CONVERT = (
    'C:\APP\ADMINISTRATOR\PRODUCT\21C\ORADATA\XE\PDBSEED\',
    'C:\APP\ADMINISTRATOR\PRODUCT\21C\ORADATA\XE\SA_TO_DELETE_PDB_27399\'
    );
```
![create pdb to delete](https://github.com/sandra2303/plsql-Pluggable-Database-Creation-Deletion-OEM-Sandrine-Uwimbabazi/blob/main/screenshots/create%20pdb%20to%20delete.PNG)

---
#### To Close

#### SQL Code
```sql
 ALTER PLUGGABLE DATABASE sa_to_delete_pdb_27399 open;

```
![create pdb to delete open](https://github.com/sandra2303/plsql-Pluggable-Database-Creation-Deletion-OEM-Sandrine-Uwimbabazi/blob/main/screenshots/alter%20to%20delete%20pdb%20close.PNG)

---

#### To Delete

#### SQL Code
```sql
DROP PLUGGABLE DATABASE sa_to_delete_pdb_27399 INCLUDING DATAFILES;

```
![Drop PDB](https://github.com/sandra2303/plsql-Pluggable-Database-Creation-Deletion-OEM-Sandrine-Uwimbabazi/blob/main/screenshots/drop%20pdb.PNG)

---

### 🧱 Task 3: Oracle Enterprise Manager (OEM)

At this stage, the database was linked to Oracle Enterprise Manager to enable visual monitoring and administration. The dashboard displays live data on system performance, resource usage, and connected users.

![OEM](https://github.com/sandra2303/plsql-Pluggable-Database-Creation-Deletion-OEM-Sandrine-Uwimbabazi/blob/main/screenshots/oem%20dasboard.PNG)


---

### 🧱 Conclusion

In conclusion, this assignment helped me understand how to create, delete, and monitor pluggable databases in Oracle.
Using both SQL commands and Oracle Enterprise Manager (OEM) improved my practical skills in database management and performance monitoring.
The successful creation and management of sa_pdb_27399 proved that the Oracle Multitenant setup works correctly.




