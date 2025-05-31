# SQLite Cheat-Sheet

## Connect to SQLite

| Command | Description |
| --- | --- |
| `sqlite3 <db>` | Connect to a SQLite database |

## SQLite CLI Commands

| Command | Description |
| --- | --- |
| `.databases` | List all databases |
| `.tables` | List all tables in the current database |
| `.schema <table>` | Show the schema of a table |
| `.indexes <table>` | List all indexes in a table |
| `.show` | Show the current settings |
| `.help` | Show help information |
| `.shell <command` | Run a shell command |
| `.exit` | Quit SQLite |

## Backup and Restore

| Command | Description |
| --- | --- |
| `.backup <file>` | Backup the current database to a file |
| `.restore <file>` | Restore a database from a file |
| `.dump` | Dump the database as SQL statements |

# MySQL Cheat-Sheet


## Connect to MySQL

| Command | Description |
| --- | --- |
| `mysql -u root -p` | Connect to MySQL as root user |
| `mysql -u <user> -p` | Connect to MySQL as a specific user |
| `mysql -u root -p -h <host>` | Connect to MySQL on a specific host |

## Backup and Restore

| Command | Description |
| --- | --- |
| `mysqldump -u root -p <database> > backup.sql` | Backup a database to a file |
| `mysql -u root -p <database> < backup.sql` | Restore a database from a file |

# PostgreSQL Cheat-Sheet

## Connect to PostgreSQL

| Command | Description |
| --- | --- |
| `psql -U postgres` | Connect to PostgreSQL as the `postgres` user |
| `psql -U <user> -d <database>` | Connect to PostgreSQL as a specific user and database |
| `psql -U <user> -d <database> -h <host>` | Connect to PostgreSQL on a specific host |

## PostreSQL CLI Commands

| Command | Description |
| --- | --- |
| `\c <database>` | Connect to a specific database |
| `\password <user>` | Change password for a specific user |
| `\l` | List all databases |
| `\d+` | Show detailed information about various database objects |
| `\dt` | List all tables in the current database |
| `\du` | List all users |
| `\df` | List all functions |
| `\dv` | List all views |
| `\dn` | List all schemas |
| `\dp` | List all permissions |
| `\di` | List all indexes |
| `\ds` | List all sequences |
| `\d+` | Show detailed information about various database objects |
| `\q` | Quit psql |
| `\x` | Toggle expanded output |

# SQL Cheat-Sheet

## Data Definition Language (DDL)

| Command | Description |
| --- | --- |
| `CREATE DATABASE <db>` | Create a new database |
| `DROP DATABASE <db>` | Delete a database |
| `CREATE TABLE <table> (<column_1> <column_1_type>, <column_2> <column_2_type>)` | Create a new table |
| `DROP TABLE <table>` | Delete a table |
| `ALTER TABLE <table> ADD COLUMN <column> <column_type>` | Add a new column to a table |
| `ALTER TABLE <table> DROP COLUMN <column>` | Remove a column from a table |
| `ALTER TABLE <table> RENAME COLUMN <column> TO <new_column>` | Rename a column in a table |
| `ALTER TABLE <table> RENAME TO <new_column>` | Rename a table |
| `TRUNCATE TABLE <table>` | Remove all rows from a table |
| `CREATE INDEX INDEXNAME ON <table> (<column>)` | Create an index on a table |
| `DROP INDEX INDEXNAME` | Remove an index from a table |

## Data Manipulation Language (DML)

| Command | Description |
| --- | --- |
| `INSERT INTO <table> (<column_1>, <column_2>) VALUES (<value_1>, <value_2>)` | Insert a new row into a table |
| `SELECT * FROM <table>` | Retrieve all rows from a table |
| `UPDATE <table> SET <column_1> = <value_1> WHERE <column_2> = <value_2>` | Update rows in a table |
| `DELETE FROM <table> WHERE <column> = <value>` | Delete rows from a table |

## Data Query Language (DQL)

| Command | Description |
| --- | --- |
| `SELECT <column_1>, <column_2> FROM <table>` | Retrieve specific columns from a table |
| `SELECT * FROM <table> WHERE <column> = VALUE` | Retrieve rows that match a condition |
| `SELECT * FROM <table> ORDER BY <column>` | Retrieve rows sorted by a column |
| `SELECT * FROM <table> LIMIT N` | Retrieve the first N rows from a table |
| `SELECT * FROM <table> OFFSET N` | Retrieve rows starting from the Nth row |
| `SELECT * FROM <table> JOIN <table_2> ON <table_1>.<column_1> = <table_2>.<column_2>` | Retrieve rows from two tables that match a condition |
| `SELECT * FROM <table> UNION SELECT * FROM <table_2>` | Retrieve rows from two tables without duplicates |
| `SELECT * FROM <table> GROUP BY <column>` | Group rows that have the same value in a column |
| `SELECT * FROM <table> HAVING COUNT(<column>) > N` | Filter grouped rows that have more than N rows |
| `SELECT * FROM <table> WHERE <column> IN (<value_1>, <value_2>)` | Retrieve rows where a column value matches any value in a list |
| `SELECT * FROM <table> WHERE <column> BETWEEN <value_1> AND <value_2>` | Retrieve rows where a column value is within a range |
| `SELECT * FROM <table> WHERE <column> LIKE '<value>%'` | Retrieve rows where a column value matches a pattern |
| `SELECT * FROM <table> WHERE <column> IS NULL` | Retrieve rows where a column value is NULL |
| `SELECT * FROM <table> WHERE <column> IS NOT NULL` | Retrieve rows where a column value is not NULL |

## Data Control Language (DCL)

| Command | Description |
| --- | --- |
| `GRANT PERMISSIONS ON <table> TO <user>` | Grant permissions to a user |
| `REVOKE PERMISSIONS ON <table> FROM <user>` | Revoke permissions from a user |

## Transaction Control Language (TCL)

| Command | Description |
| --- | --- |
| `BEGIN TRANSACTION` | Start a new transaction |
| `COMMIT` | Save changes to the database |
| `ROLLBACK` | Discard changes to the database |
| `SAVEPOINT <savepoint>` | Create a savepoint in a transaction |
| `ROLLBACK TO SAVEPOINT <savepoint>` | Rollback to a savepoint in a transaction |
| `RELEASE SAVEPOINT <savepoint>` | Remove a savepoint in a transaction |

## System Commands

| Command | Description |
| --- | --- |
| `SHOW DATABASES` | List all databases |
| `SHOW TABLES` | List all tables in the current database |
| `SHOW COLUMNS FROM <table>` | List all columns in a table |
| `SHOW INDEXES FROM <table>` | List all indexes in a table |
| `SHOW CREATE TABLE <table>` | Show the SQL statement that creates a table |
| `DESCRIBE <table>` | Show the structure of a table |
| `EXPLAIN SELECT * FROM <table>` | Show the execution plan of a query |
| `SET autocommit = 0` | Disable autocommit mode |
| `SET autocommit = 1` | Enable autocommit mode |
| `SET FOREIGN_KEY_CHECKS = 0` | Disable foreign key checks |

## User Commands

| Command | Description |
| --- | --- |
| `CREATE <user> '<user>'@'<host>' IDENTIFIED BY '<password>'` | Create a new user |
| `DROP <user> '<user>'@'<host>'` | Delete a user |
| `ALTER <user> '<user>'@'<host>' IDENTIFIED BY '<password>'` | Change password for a user |
| `GRANT ALL PRIVILEGES ON <db> TO '<user>'@'<host>'` | Grant all privileges to a user |
| `REVOKE ALL PRIVILEGES ON <db> FROM '<user>'@'<host>'` | Revoke all privileges from a user |
| `FLUSH PRIVILEGES` | Reload privileges from the grant tables |

## Backup and Restore

| Command | Description |
| --- | --- |
| `pg_dump <database> > backup.sql` | Backup a database to a file |
| `psql <database> < backup.sql` | Restore a database from a file |
