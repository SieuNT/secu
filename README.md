# secu
@author: NguyenTuanSieu
@email: dev.phpjs@gmail.com

### Reset password root
```
$>mysqld_safe --skip-grant-tables
$>mysql -uroot
$>ALTER USER 'root'@'localhost' IDENTIFIED BY 'MrSi3u@#!';
----------or-----------
$>UPDATE mysql.user SET authentication_string = PASSWORD('MrSi3u@#!'), password_expired = 'N' WHERE User = 'root' AND Host = 'localhost';
$>FLUSH PRIVILEGES;
--------MySQL 5.7.5 and earlier
$>SET PASSWORD FOR 'root'@'localhost' = PASSWORD('MrSi3u@#!');
