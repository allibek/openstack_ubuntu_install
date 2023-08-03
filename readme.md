```
/etc/hosts
10.254.60.101 controller1
10.254.60.102 compute1
```


apt install chrony
add-apt-repository cloud-archive:antelope
apt install mariadb-server python3-pymysql

/etc/mysql/mariadb.conf.d/99-openstack.cnf
[mysqld]
bind-address = 10.254.60.101
default-storage-engine = innodb
innodb_file_per_table = on
max_connections = 4096
collation-server = utf8_general_ci
character-set-server = utf8

service mysql restart
mysql_secure_installation


