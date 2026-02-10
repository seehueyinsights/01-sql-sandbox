# SQLite Database - Querying for Environemntal Monitoring Analysis

## 📖 Overview
This notebook is a simple data analysis using SQL 
- connects to a local SQLite database URL
- perform database query using SQL
- recommend actions on handling certain outliers 

The queries were written for SQLite database.

## 🛠 Features
- **Remote Access:** Downloads database files directly from a URL.
- **Smart Memory Management:** Uses the `tempfile` library to process the database without permanently saving the `.db` file to your local disk.
- **Dynamic Introspection:** Automatically queries `sqlite_master` to find all table names, rather than hard-coding them.
- **Automated Export:** Loops through every table found and converts it to a clean CSV format.

## 📦 Method & Functions Used
- `sqlite3` (Database connection)
- CASE ... WHEN
- Conditons: WHERE, IN, LIKE
- Window functions
- CTE
- Create View

## ⚙️ Logic & Methodology
1.  **Correlated Query:** A correlated query logic to determine the Median for a population to act as missing function in SQLlite.
2.  **Create View:** Instead of quering the database multiple times, the view allows the queried data to be re-used for subsequent queries.
3.  **Case .. When:** This allows Conditional scenarios to be built, which is used to tag row data with categorical information and add comments.
4.  **Data Extraction:** 
    - Connects to the local SQLite database.
    - Selects based on query statement.
    - Closes the connection to the database.

## 🚀 How to Run

### Prerequisites
Make sure you have the folder named `data` containing the SQLite database in the same directory as the script, or the export will fail.
