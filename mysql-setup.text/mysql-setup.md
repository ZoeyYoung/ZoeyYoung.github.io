Title: [安装配置] MySQL
Date: 2013-10-06
Tags: Ubuntu,Linux,安装,MySQL
Slug: mysql-setup
Author: Zoey Young
Summary: MySQL

### Ubuntu

安装: `sudo apt-get install mysql-server`

额外的一些包也会提示装上.

安装过程会给**root**用户创建密码

作为测试时我会用**123456**(有时会忘了...实验环境.)

装好后访问: `mysql -uroot -p123456` 就可以在命令行中操作数据库

安装使用**phpmyadmin**: `sudo apt-get install phpmyadmin`

添加链接:

    ~$ cd /var/www/
    /var/www$ sudo ln -s /usr/share/phpmyadmin/

打开页面: http://127.0.0.1/phpmyadmin/

用户名: root 密码: 123456

备份: `mysqldump -uroot -p123456 test>test.sql`

恢复: `mysql -uroot -p123456 test<test.sql`

[MySQL安装指南](http://wiki.ubuntu.org.cn/MySQL安装指南)