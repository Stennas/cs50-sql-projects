# 🗃️ Harvard CS50: SQL Project Exercises

This repository contains my personal solutions and practice exercises from Harvard's **CS50's Introduction to Databases with SQL**.

The course dives deep into the fundamentals of relational databases, querying with SQL, and structuring data using best practices. Each folder represents a standalone mini-project or problem set involving real-world data and scenarios.

---

## ✅ Skills & Concepts Covered

- Relational database design
- Normalization and keys
- Writing advanced SQL queries (JOINs, GROUP BY, HAVING, etc.)
- Creating, updating, and deleting tables and records
- SQL functions (e.g., `AVG()`, `COUNT()`, `CASE`)
- Subqueries and nested queries
- Triggers and transactions
- Indexing and performance optimization

---

## 📁 Project Structure

| Folder | Description |
|--------|-------------|
| `fiftyville/` | Track a suspect across multiple tables using complex SQL joins and subqueries |
| `movies/`     | Query a movie database with filtering, aggregation, and logical conditions |
| `songs/`      | Use JOINs and sorting to analyze music data |
| `airline/`    | Normalize airline passenger data and practice schema design |
| `pizza/`      | Work with many-to-many relationships and inventory logic |
| `university/` | Query students, courses, and professors using multi-table queries |
| `trigger-practice/` | Implement SQL triggers for automated changes on update/delete |

> 📌 Each folder includes `.sql` scripts used to solve the challenge, and in some cases `.db` SQLite database files used for testing.

---

## 💡 Sample Query (from `fiftyville/`)
```sql
SELECT name FROM people
JOIN passengers ON people.passport_number = passengers.passport_number
WHERE flight_id IN (
  SELECT id FROM flights WHERE origin = 'Fiftyville'
)
AND seat = '3A';


