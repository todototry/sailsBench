# sailsBench

a [Sails](http://sailsjs.org) application

usage (test performance of sails in single-node mode ):

1. cd ROOT_DIR_Of_This_App
2. npm install
3. cd /etc/init.d/ && ./mysql start
4. 进入mysql： create database sailsBench;  
5. sails lift
6. 重新进入mysql, 然后将一条数据insert进入Users表中。INSERT INTO `sailsbench`.`user` (`name`, `wingspan`, `wingspanUnits`, `id`, `createdAt`, `updatedAt`) VALUES ('todotory', '18.8', 'cm', NULL, NULL, NULL);
7. 使用ab工具，ab -n 10000 -c 100 http://localhost:1337/User/find/1

usage (test performance of sails in cluster mode with pm2):

1. npm install -g pm2

2. pm2 start app.js -i 4 -f  (force to start 4 nodes in cluster mode.)

3. pm2 stop app

4. pm2 kill (stop the pm2 deamon if you want to start in fork mode.)

