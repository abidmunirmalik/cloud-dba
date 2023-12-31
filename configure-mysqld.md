## CONFIGURE MYSQL SERVER ON DEBIAN SYSTEM

### CREATE CUSTOM DIRECTORY FOR MYSQL CONFIGURATION
```
mkdir /etc/mysql/gdp
```

### COPY EXISTING CONFIGURATION FILES
```
cp /etc/mysql/mysql.conf.d/mysqld.cnf /etc/mysql/gdp/
```

### MODIFY /etc/mysql/my.cnf
```
vim /etc/mysql/my.cnf
!includedir /etc/mysql/gdp/
```

### REMOVE EXISTING CONFIGURATION FILES
```
rm -f /etc/mysql/debian-start && rm -f /etc/mysql/debian.cnf
rm -f /etc/mysql/my.cnf.fallback && rm -f /etc/mysql/mysql.cnf
rm -rf /etc/mysql/conf.d && rm -rf /etc/mysql/mysql.conf.d
```

### RESTART MYSQL SERVICE TO VERIFY
```
systemctl restart mysql.service
```
