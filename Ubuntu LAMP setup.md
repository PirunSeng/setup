## Install PHP

```
sudo apt install zip unzip software-properties-common
sudo add-apt-repository ppa:ondrej/php
sudo apt install -y php7.4 php7.4-gd php7.4-mbstring php7.4-xml php-zip
```


## Install Apache2

```
sudo apt install apache2 libapache2-mod-php7.4
```

## Install Mysql

```
sudo apt install mysql-server php7.4-mysql
```

## Install Composer

```
curl -sS https://getcomposer.org/installer | php
sudo mv composer.phar /usr/local/bin/composer
sudo chmod +x /usr/local/bin/composer
```

### Assume we have mysql running

## Create database

### Root user
```
mysql -u root -p
```

### Non root user
```
sudo mysql
```

### Then

```
CREATE DATABASE dbname;
CREATE USER 'dbuser'@'dbhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON * . * TO 'dbuser'@'dbhost';
FLUSH PRIVILEGES;
```
