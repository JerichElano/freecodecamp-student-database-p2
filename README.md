# Student Database (Part 2)

A project completed as part of freeCodeCamp's **Relational Database Certification**. The goal of this workshop is to practice advanced SQL querying techniques, including multi-table joins, conditional filtering, string pattern matching, and aggregate functions through a Bash automation script.

## 📁 Repository Contents

- `students.sql` — PostgreSQL dump containing the complete database schema and sample data for the `students`, `majors`, `courses`, and `majors_courses` tables.
- `student_info.sh` — A Bash script that runs a series of PostgreSQL queries to extract specific statistics, course lists, and student records.

## 🛠 Tech Stack & SQL Concepts

- **Database:** PostgreSQL
- **Scripting:** Bash / Shell
- **CLI Utilities:** `psql`
- **SQL Techniques Covered:**
  - `INNER JOIN`, `RIGHT JOIN`, `FULL JOIN`
  - Pattern matching (`LIKE`, `ILIKE`, wildcards)
  - Aggregations & grouping (`COUNT`, `AVG`, `ROUND`, `GROUP BY`, `HAVING`)
  - Subshell query execution with `psql`

## 🚀 How It Works

1. **Database Setup:** The database structure and default records are initialized using the `students.sql` dump file.
2. **Query Execution:** The `student_info.sh` script executes formatted SQL queries against the `students` database using `psql` and prints the structured results directly to the terminal.

## 🏃 Running Locally

To rebuild the database and run the information script on your local machine:

```bash
# 1. Create the database and import the schema/data
psql -U postgres -c "CREATE DATABASE students;"
psql -U postgres -d students < students.sql

# 2. Grant execute permissions to the script
chmod +x student_info.sh

# 3. Run the student info script
./student_info.sh
