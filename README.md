docker-mysql
============

Minimal base image for running MySQL on Docker. Example:

    $ docker run -d -p 3307:3306 -e MYSQL_ROOT_PASSWORD=xehVg1IpVhEmlwRMG theasci/mysql /usr/bin/mysqld
    da809981545f
    $ mysql -h 127.0.0.1 -P 3307 -u root -p
    Enter password:
    Welcome to the MySQL monitor.  Commands end with ; or \g.
    Your MySQL connection id is 1
    Server version: 5.5.34-0ubuntu0.12.04.1-log (Ubuntu)

    Copyright (c) 2000, 2013, Oracle and/or its affiliates. All rights reserved.

    Oracle is a registered trademark of Oracle Corporation and/or its
    affiliates. Other names may be trademarks of their respective
    owners.

    Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

    mysql>

(Example assumes MySQL client is installed on Docker host.)

Environment variables
---------------------

 - `MYSQL_ROOT_PASSWORD`: The password for the root user, set every time the server starts. Defaults to a blank password, which is handy for development, but you should set this to something in production.
