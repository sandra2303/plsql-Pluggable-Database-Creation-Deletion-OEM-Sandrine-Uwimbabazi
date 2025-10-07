# plsql-Pluggable-Database-Creation-Deletion-OEM-Sandrine-Uwimbabazi
PDB
# 🧩 Assignment 2: Database Creation, Deletion & OEM

### Student: Uwimbabazi Sandrine  
### Student ID: 27399  
### Course: Database Development with PL/SQL 
### Instructor: Eric Maniraguha  
### Submission Date: 7 October 2025  

---

## 🪄 Introduction

This project focuses on understanding and managing **Oracle Multitenant Databases**, which allow multiple pluggable databases (PDBs) to run under a single container database (CDB).  
The main goal was to practice creating, deleting, and monitoring pluggable databases using both **SQL commands** and **Oracle Enterprise Manager (OEM)**.  

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
![create PDB](https://github.com/sandra2303/plsql-Pluggable-Database-Creation-Deletion-OEM-Sandrine-Uwimbabazi/blob/main/screenshots/drop%20pdb.PNG)

---

```sql

ALTER PLUGGABLE DATABASE sa_pdb_27399 OPEN;
```
![alter open](https://github.com/sandra2303/plsql-Pluggable-Database-Creation-Deletion-OEM-Sandrine-Uwimbabazi/blob/main/screenshots/alter%20open.PNG)

---
