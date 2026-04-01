# 📊 SQLBolt Solutions: Database Fundamentals

![SQL](https://img.shields.io/badge/Language-SQL-blue.svg)
![Database](https://img.shields.io/badge/Database-SQLite-green.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)

This repository houses my personal solutions for the [SQLBolt](https://sqlbolt.com/) curriculum. It serves as a comprehensive reference for SQL syntax and relational database concepts, ranging from basic data retrieval to advanced schema management.

---

## 🎯 Learning Objectives
The primary goal of this project was to master the core principles of **Relational Database Management Systems (RDBMS)**. Through these exercises, I've developed a strong foundation in:

* **Querying:** Writing efficient `SELECT` statements with complex `WHERE` logic.
* **Relational Mapping:** Utilizing `JOIN` clauses to connect disparate data entities.
* **Data Analysis:** Summarizing datasets using aggregate functions and grouping logic.
* **Database Administration:** Managing life cycles of tables via `CREATE`, `ALTER`, and `DROP`.

---

## 📂 Curriculum Overview

| Lessons | Topic | Key Keywords |
| :--- | :--- | :--- |
| **1 - 5** | **Basic Queries** | `SELECT`, `WHERE`, `ORDER BY`, `LIMIT` |
| **6 - 9** | **Joins** | `INNER JOIN`, `LEFT JOIN`, `ON`, `USING` |
| **10 - 12** | **Aggregates** | `COUNT`, `SUM`, `MIN/MAX`, `GROUP BY`, `HAVING` |
| **13 - 15** | **CRUD Operations** | `INSERT`, `UPDATE`, `DELETE` |
| **16 - 18** | **Schema Design** | `CREATE TABLE`, `ALTER`, `DROP` |

---

## 💡 Highlighted Examples

### Complex Multi-table Join
Extracting movie titles and their ratings from two different tables where the rating exceeds a specific threshold:

```sql
SELECT movies.title, boxoffice.rating
FROM movies
JOIN boxoffice 
  ON movies.id = boxoffice.movie_id
WHERE boxoffice.rating > 8.0
ORDER BY boxoffice.rating DESC;
