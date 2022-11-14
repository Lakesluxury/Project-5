# Project-5 Documentations

## Implement a Client Server Architecture using MySQL Database Management System (DBMS)

`sudo apt install mysql-server -y`

![mysql server installation](./install%20mysql%20server.PNG)

`sudo systemctl enable mysql`

![enable mysql server](./enable%20mysql.PNG)

`sudo apt install mysql-client -y`

![mysql client installation](./install%20mysql%20client.PNG)

### Creating a new entry in ‘Inbound rules’ in ‘mysql server’ Security Groups

![ip addr show](./ip%20addy.PNG)

![new inbound rule](./ip%20addy1.PNG)

### Creating Database and User on mysql server

`sudo mysql_secure_installation`

![mysql sec instal](./mysql%20sec%20instll.PNG)

`sudo mysql -p`

### Creating a User 

`CREATE USER 'remote_user'@'%' IDENTIFIED WITH mysql_native_password BY 'Password.1';`

![create user](./create%20user.PNG)

### Creating a Database

`CREATE DATABASE test_db;`

![create db](./create%20dabase.PNG)

Grant privileges to User

`GRANT ALL ON test_db.* TO 'remote_user'@'%' WITH GRANT OPTION;`

![grant privilege](./grant.PNG)

### Flush the privileges

`FLUSH PRIVILEGES;`

![flush privileges](./flush.PNG)

### Exit mysql

### Configure MySQL server to allow connections from remote hosts

`sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf`

![connect from remote host](./connect%20from%20remotehost.PNG)

### Connection from mysql client Linux Server remotely to mysql server Database Engine without using SSH

`sudo mysql -u remote_user -h 172.31.90.223 -p`

`Show databases;`

![connection](./client%20connect%20%26%20show%20db.PNG)





