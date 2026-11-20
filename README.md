# Week 8 Assignment: MySQL Database Backup and Restore

This assignment demonstrates how to create MySQL database backups using the `mysqldump` command-line utility.

## Question 1: Create a Complete Database Backup

### Command

```bash
mysqldump -u root -p sales > sales_backup.sql
```

### Explanation

- `mysqldump` is the MySQL command-line backup utility.
- `-u root` connects to MySQL as the root user.
- `-p` tells MySQL to prompt for the password.
- `sales` is the name of the database being backed up.
- `>` saves the backup output into a file called `sales_backup.sql`.

This command creates a complete backup of the `sales` database, including its table structures and data.

Regular database backups are important because they protect data from accidental deletion, hardware failure, software errors, corruption, security incidents, and human mistakes. If data is lost or damaged, the database can be restored using the backup file.

## Question 2: Back Up All Databases

### Command

```bash
mysqldump -u root -p --all-databases > all_databases_backup.sql
```

### Explanation

- `mysqldump` is the MySQL command-line backup utility.
- `-u root` connects to MySQL as the root user.
- `-p` tells MySQL to prompt for the password.
- `--all-databases` backs up every database on the MySQL server.
- `>` saves the backup output into a file called `all_databases_backup.sql`.

This command creates a complete backup of all databases on the MySQL server.

Backing up all databases before migration is important because it preserves the entire MySQL server environment. If an error occurs during migration, the administrator can restore the databases and avoid losing application data, table structures, and important database information.
