docker-mysql
============

Minimal base image for running MySQL on Docker using the "centos" base image. Example:

    $ docker run -d -p 3307:3306 theasci/docker-mysql
    da809981545f
    $ mysql --host=127.0.0.1 --port=3307 --user=root --password=''
    Welcome to the MySQL monitor.  Commands end with ; or \g.
    Your MySQL connection id is 1
    Server version: 5.6.17-log MySQL Community Server (GPL)
    
    Copyright (c) 2000, 2014, Oracle and/or its affiliates. All rights reserved.
    
    Oracle is a registered trademark of Oracle Corporation and/or its
    affiliates. Other names may be trademarks of their respective
    owners.
    
    Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.
    
    mysql>

(Example assumes MySQL client is installed on Docker host.)

Environment variables
---------------------

 - `MYSQL_ROOT_PASSWORD`: The password for the root user, set during build time. Defaults to a blank password, which is handy for development, but you should set this to something in production.
