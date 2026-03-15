mysql> CREATE DATABASE library_404;
ERROR 1007 (HY000): Can't create database 'library_404'; database exists
mysql> USE library_404;
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| library_404        |
| mysql              |
| performance_schema |
| sys                |
| user_404           |
+--------------------+
6 rows in set (0.00 sec)

mysql> CREATE TABLE category_404 (
    ->     category_id INT AUTO_INCREMENT PRIMARY KEY,
    ->     category_name VARCHAR(100) NOT NULL
    -> );
ERROR 1050 (42S01): Table 'category_404' already exists
mysql> CREATE TABLE user_404 (
    ->     user_id INT AUTO_INCREMENT PRIMARY KEY,
    ->     name VARCHAR(100) NOT NULL,
    ->     email VARCHAR(100) UNIQUE,
    ->     role VARCHAR(50)
    -> );
Query OK, 0 rows affected (0.01 sec)

mysql> CREATE TABLE book_404 (
    ->     book_id INT AUTO_INCREMENT PRIMARY KEY,
    ->     title VARCHAR(200) NOT NULL,
    ->     author VARCHAR(100),
    ->     ISBN VARCHAR(20),
    ->     availability VARCHAR(20),
    ->     category_id INT,
    ->     
    ->     FOREIGN KEY (category_id)
    ->     REFERENCES category_404(category_id)
    -> );
Query OK, 0 rows affected (0.01 sec)

mysql> CREATE TABLE borrow_404 (
    ->     borrow_id INT AUTO_INCREMENT PRIMARY KEY,
    ->     user_id INT,
    ->     book_id INT,
    ->     borrow_date DATE,
    ->     return_date DATE,
    ->     
    ->     FOREIGN KEY (user_id)
    ->     REFERENCES user_404(user_id),
    ->     
    ->     FOREIGN KEY (book_id)
    ->     REFERENCES book_404(book_id)
    -> );
Query OK, 0 rows affected (0.01 sec)

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| library_404        |
| mysql              |
| performance_schema |
| sys                |
| user_404           |
+--------------------+
6 rows in set (0.00 sec)

mysql> USE library_404;
Database changed
mysql> SHOW TABLES;
+-----------------------+
| Tables_in_library_404 |
+-----------------------+
| book_404              |
| borrow_404            |
| category_404          |
| user_404              |
+-----------------------+
4 rows in set (0.00 sec)

mysql> show tables;
+-----------------------+
| Tables_in_library_404 |
+-----------------------+
| book_404              |
| borrow_404            |
| category_404          |
| user_404              |
+-----------------------+
4 rows in set (0.00 sec)

mysql> describe book_404;
+--------------+--------------+------+-----+---------+----------------+
| Field        | Type         | Null | Key | Default | Extra          |
+--------------+--------------+------+-----+---------+----------------+
| book_id      | int          | NO   | PRI | NULL    | auto_increment |
| title        | varchar(200) | NO   |     | NULL    |                |
| author       | varchar(100) | YES  |     | NULL    |                |
| ISBN         | varchar(20)  | YES  |     | NULL    |                |
| availability | varchar(20)  | YES  |     | NULL    |                |
| category_id  | int          | YES  | MUL | NULL    |                |
+--------------+--------------+------+-----+---------+----------------+
6 rows in set (0.01 sec)

mysql> describe borrow_404;
+-------------+------+------+-----+---------+----------------+
| Field       | Type | Null | Key | Default | Extra          |
+-------------+------+------+-----+---------+----------------+
| borrow_id   | int  | NO   | PRI | NULL    | auto_increment |
| user_id     | int  | YES  | MUL | NULL    |                |
| book_id     | int  | YES  | MUL | NULL    |                |
| borrow_date | date | YES  |     | NULL    |                |
| return_date | date | YES  |     | NULL    |                |
+-------------+------+------+-----+---------+----------------+
5 rows in set (0.00 sec)

mysql> describe category_404;
+---------------+--------------+------+-----+---------+----------------+
| Field         | Type         | Null | Key | Default | Extra          |
+---------------+--------------+------+-----+---------+----------------+
| category_id   | int          | NO   | PRI | NULL    | auto_increment |
| category_name | varchar(100) | NO   |     | NULL    |                |
+---------------+--------------+------+-----+---------+----------------+
2 rows in set (0.00 sec)

mysql> describe user_404;
+---------+--------------+------+-----+---------+----------------+
| Field   | Type         | Null | Key | Default | Extra          |
+---------+--------------+------+-----+---------+----------------+
| user_id | int          | NO   | PRI | NULL    | auto_increment |
| name    | varchar(100) | NO   |     | NULL    |                |
| email   | varchar(100) | YES  | UNI | NULL    |                |
| role    | varchar(50)  | YES  |     | NULL    |                |
+---------+--------------+------+-----+---------+----------------+
4 rows in set (0.01 sec)

mysql> 
