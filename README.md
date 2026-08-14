# Database Management Systems Laboratory

[![SQL](https://img.shields.io/badge/Language-SQL%20%7C%20PL%2FSQL-CC292B.svg)](#)
[![Oracle](https://img.shields.io/badge/Database-Oracle%2019c%20%7C%2021c-F80000.svg)](https://www.oracle.com/database/)
[![MongoDB](https://img.shields.io/badge/NoSQL-MongoDB%206.0%2B-47A248.svg)](https://www.mongodb.com/)
[![License](https://img.shields.io/badge/License-Academic-lightgrey.svg)](#)

## 1. Project Title
**Database Management Systems Laboratory: Relational Schema Design, Advanced SQL, PL/SQL Programmability, and NoSQL MongoDB Administration**

## 2. Project Overview
This repository contains a full 16-experiment laboratory portfolio for **Database Management Systems (DBMS)**. The curriculum spans foundational relational database concepts, Data Definition Language (DDL), Data Manipulation Language (DML), complex relational querying (joins, nested subqueries, aggregations), database object management, procedural SQL programming (PL/SQL blocks, functions, procedures, explicit cursors, database triggers), database security/access control (DCL), and modern document-oriented NoSQL querying in MongoDB.

Each laboratory record is systematically compiled with relational schemas, formal problem descriptions, executable SQL and PL/SQL scripts, query execution plans, and documented query output verification.

---

## 3. Objectives
- Design and implement normalized relational schemas utilizing integrity constraints (Primary Key, Foreign Key, Check, Not Null, Unique).
- Execute comprehensive DML operations and transaction control commands (COMMIT, ROLLBACK, SAVEPOINT).
- Master advanced single-row transformation functions, conditional logic (CASE, DECODE), and multi-table joins (inner, outer, cross, natural).
- Implement procedural logic using Oracle PL/SQL, including stored procedures, stored functions, parameter passing (`IN`, `OUT`, `IN OUT`), and explicit cursors.
- Enforce business logic and automated audit logging via row-level and statement-level database triggers.
- Administer database security using Data Control Language (DCL): user creation, system and object privilege delegation, and role-based access control (RBAC).
- Explore non-relational document data stores by querying, filtering, and aggregating BSON documents in MongoDB.

---

## 4. Key Features
- **End-to-End Relational Lifecycle**: Complete DDL and DML scripts from schema specification to advanced multi-table queries.
- **Advanced Querying**: Multi-table inner/outer joins, correlated subqueries, set operations, and group aggregations using `GROUP BY` and `HAVING`.
- **Procedural Database Programmability**: Production PL/SQL units utilizing cursor attributes (`%FOUND`, `%NOTFOUND`, `%ROWCOUNT`), conditional control flows, and user-defined exception handling.
- **Automated Trigger Mechanisms**: Reactive database triggers maintaining referential integrity and tracking transactional changes.
- **Enterprise Database Objects**: Sequences for primary key generation, views for data abstraction, and B-tree indexes for query optimization.
- **Hybrid Relational & NoSQL Coverage**: Direct architectural comparison between tabular relational schemas in Oracle and flexible document schemas in MongoDB.

---

## 5. Technologies Used
- **Relational DBMS**: Oracle Database (SQL*Plus, Oracle SQL Developer)
- **Procedural Extensions**: Oracle PL/SQL
- **NoSQL DBMS**: MongoDB (Mongo Shell / mongosh)
- **Data Definition & Query Languages**: ANSI SQL-92 / SQL:1999, JSON / BSON Query Syntax
- **Documentation**: Comprehensive PDF Laboratory Records

---

## 6. Project Structure
```text
DATABASE-MANAGEMENT-SYSTEMS-COURSE/
│
├── EXP_1.pdf          # Experiment 1: Base Table Creation and DML Operations (MY_EMPLOYEE)
├── Exp_2.pdf          # Experiment 2: Data Manipulation, Projections, and Filtering
├── Exp_03.pdf         # Experiment 3: Basic SQL SELECT Statements, Concatenations & Aliases
├── Exp_4_.pdf         # Experiment 4: Restricting and Sorting Data (WHERE, ORDER BY)
├── Exp_5.pdf          # Experiment 5: Single-Row SQL Functions (String, Numeric, Date)
├── Exp_6.pdf          # Experiment 6: Conversion Functions and Conditional Expressions (CASE/DECODE)
├── Exp_7.pdf          # Experiment 7: Reporting Aggregated Data using Group Functions
├── Exp_8.pdf          # Experiment 8: Multi-Table Joins (Equijoins, Outer Joins, Self Joins)
├── Exp_9.pdf          # Experiment 9: Single-Row and Multiple-Row Subqueries
├── Exp_10.pdf         # Experiment 10: Aggregating Data using GROUP BY and HAVING Clauses
├── Exp_11.pdf         # Experiment 11: PL/SQL Anonymous Blocks, Variables, and Control Structures
├── Exp_12.pdf         # Experiment 12: Working with Explicit Cursors, Procedures, and Functions
├── Exp_13.pdf         # Experiment 13: Database Triggers (Row-Level, Statement-Level & Auditing)
├── Exp_14.pdf         # Experiment 14: MongoDB Document Ingestion, Filtering, and Aggregation
├── Exp_15.pdf         # Experiment 15: Database Objects (Sequences, Views, Indexes, Synonyms)
├── Exp_16.pdf         # Experiment 16: Controlling User Access, Privileges, and Roles (DCL)
│
└── README.md
```

---

## 7. Installation and Prerequisites
### Prerequisites
- Oracle Database (Express Edition XE or Enterprise Edition) or Oracle Live SQL
- MongoDB Community Server & MongoDB Shell (`mongosh`)

### Connecting to Oracle SQL
```sql
-- Connect via SQL*Plus
sqlplus username/password@localhost:1521/XEPDB1
```

### Connecting to MongoDB
```bash
mongosh "mongodb://localhost:27017"
```

---

## 8. Execution Instructions
### Executing Oracle SQL / PL/SQL Scripts
1. Launch `sqlplus` or Oracle SQL Developer.
2. Enable console output for PL/SQL blocks:
   ```sql
   SET SERVEROUTPUT ON;
   ```
3. Execute the desired experiment script (e.g., `Exp_11.pdf` PL/SQL procedures):
   ```sql
   @Exp_11.sql
   ```

### Executing MongoDB Queries
1. In `mongosh`, select or initialize the database:
   ```javascript
   use test_db;
   ```
2. Run document queries directly from `Exp_14.pdf`:
   ```javascript
   db.restaurants.find({
     $or: [
       { cuisine: { $nin: ["American", "Chinese"] } },
       { name: /^Wil/i }
     ]
   });
   ```

---

## 9. Implementation and Methodology

| Exp No. | Experiment Title | Core SQL / PL/SQL Commands & Concepts | Schema / Domain |
|---|---|---|---|
| **01** | Base Table DDL & DML | `CREATE TABLE`, `INSERT INTO`, `UPDATE`, `DELETE`, `COMMIT` | `MY_EMPLOYEE` Table |
| **02** | Data Manipulations | Projection, Selection, Predicate Filtering, Managerial Hierarchy | HR Schema / Employees |
| **03** | Basic SQL Projections | `DESC`, `SELECT DISTINCT`, String Concatenation `\|\|`, Column Aliasing | HR Departments & Employees |
| **04** | Sorting & Restricting | `BETWEEN ... AND`, `IN (...)`, `LIKE '%pattern%'`, `IS NULL`, `ORDER BY` | Employee Salaries & Dates |
| **05** | Single-Row Functions | `LOWER`, `UPPER`, `SUBSTR`, `INSTR`, `ROUND`, `TRUNC`, `SYSDATE`, `MONTHS_BETWEEN` | String & Date Analytics |
| **06** | Conversion & Conditionals | `TO_CHAR`, `TO_DATE`, `NVL`, `NVL2`, `COALESCE`, `CASE ... WHEN`, `DECODE` | Formatted Payroll Reports |
| **07** | Group Functions | `AVG`, `SUM`, `MIN`, `MAX`, `COUNT(*)`, `VARIANCE`, `STDDEV` | Department Compensation |
| **08** | Multi-Table Joins | `NATURAL JOIN`, `JOIN ... ON`, `LEFT/RIGHT/FULL OUTER JOIN`, `CROSS JOIN` | Employees, Departments, Locations |
| **09** | Subqueries | Single-row (`=`), Multi-row (`IN`, `ANY`, `ALL`), Correlated Subqueries | Hierarchical Salary Queries |
| **10** | Group Aggregations | `GROUP BY`, `HAVING` filter clause, Nested aggregate evaluations | Departmental Salary Statistics |
| **11** | PL/SQL Fundamentals | Anonymous Blocks, `%TYPE`, `IF-THEN-ELSIF`, `DBMS_OUTPUT.PUT_LINE` | Incentive Calculation |
| **12** | Cursors & Procedures | Explicit Cursors (`OPEN/FETCH/CLOSE`), `CREATE PROCEDURE`, `CREATE FUNCTION` | Factorial, Book Inventory |
| **13** | Database Triggers | `BEFORE/AFTER INSERT OR DELETE`, Row-level `:OLD`/`:NEW`, Referential Integrity | Cascading Audits |
| **14** | MongoDB NoSQL Queries | `db.collection.find()`, `$or`, `$nin`, Regex `^Wil/i`, Projections | Restaurant Directory Collection |
| **15** | Database Objects | `CREATE SEQUENCE`, `CREATE VIEW`, `CREATE INDEX`, `CREATE SYNONYM` | Sequence IDs, Virtual Tables |
| **16** | Database Security (DCL) | `CREATE USER`, `GRANT CREATE SESSION`, `WITH GRANT OPTION`, `CREATE ROLE` | Role-Based Access Control |

---

## 10. Results and Outputs
- **Relational Integrity**: Enforced primary key and foreign key constraints across `department` and `employee` tables, preventing orphan records.
- **Complex Query Execution**: Generated multi-table joined reports accurately linking employee compensation, departmental classifications, and geographical locations.
- **PL/SQL Automation**: Verified procedural execution of stored functions (calculating factorials and tax incentives) and stored procedures with `IN OUT` parameters.
- **Trigger Validation**: Successfully caught unauthorized delete attempts on parent records with active child relations, raising descriptive application errors (`RAISE_APPLICATION_ERROR`).
- **NoSQL Flexibility**: Queried complex nested JSON documents in MongoDB using regex filtering and logical negation operators with sub-millisecond retrieval.

---

## 11. Screenshots and Visual Documentation
The experiment records, schema definitions, and query execution outputs are compiled in high-fidelity PDF records within the repository:
- `EXP_1.pdf` through `Exp_13.pdf`, `Exp_15.pdf`, `Exp_16.pdf`: SQL and PL/SQL scripts with table dumps.
- `Exp_14.pdf`: MongoDB queries and BSON document query output listings.

---

## 12. Learning Outcomes
- Acquired end-to-end expertise in relational database modeling, schema normalization, and integrity constraint enforcement.
- Gained fluency in writing performant SQL queries combining joins, nested subqueries, and analytical group functions.
- Developed backend database programming skills in Oracle PL/SQL, writing modular, maintainable procedures, functions, and triggers.
- Understood database administration essentials including user privileges, security roles, indexes, and transactions.
- Developed an understanding of the trade-offs between ACID-compliant relational systems (Oracle) and schema-flexible NoSQL systems (MongoDB).

---

## 13. Future Improvements
- Package the SQL and PL/SQL scripts into standalone `.sql` files with automated initialization and teardown scripts.
- Integrate object-relational mapping (ORM) with Python (`SQLAlchemy`) or Java (`Hibernate`).
- Add performance profiling using Oracle `EXPLAIN PLAN` and MongoDB `.explain("executionStats")` to analyze index utilization and cost.

---

## 14. Author
**Rohita M**  
- **GitHub**: [@rohitam26](https://github.com/rohitam26)  
- **Academic Program**: B.E. Artificial Intelligence and Machine Learning  
- **Institution**: Rajalakshmi Engineering College  
