# sailsBench

a [Sails](http://sailsjs.org) application

usage:

1. cd ROOT_DIR_Of_This_App
2. npm install
3. cd /etc/init.d/ && ./mysql start
4. 进入mysql： create database sailsBench;  
5. sails lift
6. 重新进入mysql, 然后将一条数据insert进入Users表中。
7. 使用ab工具，ab -n 10000 -c 100 http://localhost:1337/User/find/1
