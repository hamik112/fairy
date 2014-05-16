Fairy
=====

An automated Nginx based web server installer for Cloud Services such as DigitalOcean

## Features
* Written for Ubuntu 14.04 LTS
* Installs Nginx
* Create virtual server block for nginx
* Installs PHP, PHP APC, PHP Curl etc.
* Supports PHP Fast Process Manager (php-fpm)
* Installs Memcached
* Installs Database (MariaDB / MySQL)
* Installs Content Management System - Joomla
* Configures and Strengthens SSH
* Activates Firewall

## How to use Fairy
Specify the values for the following variables to customize how the program should configure the webserver
* SITENAME - Specify the site name of the first (default) website (e.g. SITENAME='akashmitra.com')
* SITEUSER - Specify the username of the default website (e.g., SITEUSER='akashmitra')
* PHP_SESSION_HANDLER - Whether the PHP session data should be stored in files or in memcached location. Currently it does not support database. (e.g. PHP_SESSION_HANDLER="files")
* MEMCACHED_TCP_PORT - The TCP port that memcached should use for communication. (e.g., MEMCACHED_TCP_PORT="29216"). Leave this variable blank if you wish memcached to use Unix domain socket 
* SESSION_SAVE_PATH - Specify PHP session.save_path when PHP_SESSION_HANDLER is neither files or memcached. This can be left empty if PHP_SESSION_HANDLER is files or memcached.
* SSH_PORT -  specify an SSH connection port. Leave this blank if you want to continue with the default port (22)

## How to Execute Fairy
Login as root and execute the following commands
```
# curl -O https://raw.githubusercontent.com/akash-mitra/fairy/master/fairy.sh
# chmod +x fairy.sh
# ./fairy.sh
```

## How to see the result
Once fairy execution is complete, it will generate following files under `/root/` directory

1. /root/you_must_read_me.txt
2. /root/system_change_log

Please read the file `you_must_read_me.txt` for further valuable information

