# Tech Docs 

This documents contains my daily search on StackOverflow as a software engineer. I don't know how many repititve things and commands I search everyday. That's the reason i want to reduce my stackoverflow search while coding. 

### 1. How To Import MYSQL Dump In Local system ?

Check whether mysql is installed and running on your system.

```
which mysql
```

```
sudo service mysql status
```

**First Create a new database in mysql before importing**. 

1. Login to MYSQL on your local system.

```
mysql -u USER_NAME -p
```

2. Create new Database.(In MYSQL shell)

```
CREATE database DB_NAME
```

3. Now, Import Your mysql dump.

```
mysql -u MYSQL_USERNANME -p DB_NAME < DB_PATH
```

### 2. How To Create Dump Of MYSQL DB ? 

```
 mysqldump -h HOST_NAME -u USER_NAME -p DB_NAME > DUMP_NAME.sql
 ```

 If you get this **mysqldump: Got error: 1044**
 Access deined when using lock tables.

Run this command by adding ***--single-transaction***

 ```
  mysqldump --single-transaction -h HOST_NAME -u USER_NAME -p DB_NAME > DUMP_NAME.sql
```
