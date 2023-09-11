## DISBLE MYSQL AUTO-START INIT SCRIPT ON DEBIAN-BASED SYSTEMS


### DISABLE MYSQL INIT SCRIPT
```
mv /etc/init.d/mysql ~
```

### REMOVE DEBIAN SCRIPTS
```
mv /etc/mysql/debian.cnf ~ && mv /etc/mysql/debian-start ~
```

### MANAGE MYSQL SERVICE UNDER SYSTEMD
```
systemctl status mysql.service
```

### RESTART MYSQL SERVICE UNDER SYSTEMD
```
systemctl stop mysql.service && systemctl start mysql.service
```

### VERIFY MYSQL SERVICE
```
journalctl -u mysql.service
```
