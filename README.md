# Day-52-100-Days-challenge-in-cybersecurity-
## Day 52: SQL Command Types (DDL & DML) 🗄️

### 📌 Overview
Today's focus was on the classification of SQL commands. In cybersecurity, understanding these categories is essential for identifying misconfigurations and potential injection vulnerabilities.

### 🗂️ SQL Command Categories
| Category | Role | Key Commands |
| :--- | :--- | :--- |
| **DDL** | **The Architect** (Structure) | `CREATE`, `DROP`, `ALTER`, `TRUNCATE` |
| **DML** | **The Tenant** (Data) | `INSERT`, `UPDATE`, `DELETE` |
| **DQL** | **The Librarian** (Query) | `SELECT` |
| **DCL** | **The Security Guard** (Control)| `GRANT`, `REVOKE` |
| **TCL** | **The Manager** (Transaction) | `COMMIT`, `ROLLBACK` |

### 🛡️ Security Perspective: The DDL vs. DML Divide
In a secure production environment, the application's database user should **never** have DDL privileges. 

* **The Risk:** If an attacker successfully executes a SQL Injection (SQLi) attack and the database user has `DROP` or `ALTER` permissions, they can permanently destroy the data structure or create backdoors by adding new admin columns.
* **The Fix:** Implement the **Principle of Least Privilege**. Ensure the web user can only manipulate data (DML), not define the database structure (DDL).

---
*Part of my #100DaysOfHacking Challenge.*
