
# SQLite Database with Python



This project demonstrates how to use **SQLite with Python** to create, manage, and query a relational database. It walks through the full workflow of connecting to a database, creating tables, inserting data, and retrieving results using SQL queries.

---

## 📌 Project Overview

The goal of this project is to understand how Python interacts with a relational database using the built-in `sqlite3` module.

The workflow includes:

1. Establishing a connection to a database  
2. Creating tables  
3. Inserting records  
4. Querying data  
5. Closing the connection properly  

---

## 🧱 Database Setup

A SQLite database file is created:

```

INSTRUCTOR.db

````

SQLite stores the entire database in a single file, making it lightweight and easy to use without a server.

---

## 🔌 Connecting to the Database

A connection is created using:

```python
import sqlite3
conn = sqlite3.connect("INSTRUCTOR.db")
````

This allows Python to communicate with the database.

A cursor is then created to execute SQL commands:

```python
cursor = conn.cursor()
```

---

## 🏗️ Creating Tables

Tables are created using SQL commands:

```sql
CREATE TABLE INSTRUCTOR (...)
```

This defines the structure of the data, including columns such as name, ID, or department.

---

## ➕ Inserting Data

Data is added using `INSERT` statements:

```sql
INSERT INTO INSTRUCTOR VALUES (...)
```

Each row represents one record in the table.

After inserting data, changes must be saved:

```python
conn.commit()
```

---

## 🔍 Querying Data

Data is retrieved using SQL queries:

```sql
SELECT * FROM INSTRUCTOR;
```

This returns all rows in the table.

You can also filter or aggregate data using conditions.

---

## 📤 Displaying Results

Query results are fetched in Python:

```python
rows = cursor.fetchall()
```

These results can then be printed or processed further.

---

## 🔚 Closing the Connection

Once operations are complete, the connection should be closed:

```python
conn.close()
```

This ensures resources are released properly.

---

## 📊 Key Concepts

* SQLite is a **serverless database**
* Python interacts with it using **DB-API**
* Data operations follow:

  * connect → execute → commit → close
* SQL is used for all database operations

---

## 🧩 File Structure

```
SQLite-database-python.ipynb   # main notebook
INSTRUCTOR.db                 # database file
INSTRUCTOR.db-journal         # SQLite transaction log
README.md                     # project documentation
```

---

## ⚠️ Notes

* The `.db-journal` file is automatically created by SQLite for transaction safety
* It can be ignored in most cases
* Always commit changes before closing the connection

---

## 🚀 Future Improvements

* Add more complex queries (JOIN, GROUP BY)
* Build a simple UI to interact with the database
* Integrate with a web application
* Use parameterized queries for security


