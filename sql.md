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

## Backup and Restore

| Command | Description |
| --- | --- |
| `pg_dump <database> > backup.sql` | Backup a database to a file |
| `psql <database> < backup.sql` | Restore a database from a file |
