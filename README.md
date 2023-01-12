# covid19 map web url
http://47.108.179.63:3000/

# REACT-NODEJS-MYSQL-DOCKER 

Tutorial
---------

[Docker compose : NodeJS and MySQL app with React in a docker](http://www.bogotobogo.com/DevOps/Docker/Docker-React-Node-MySQL-App.php) 

step 1
---
在专案的根目录下执行 (-d 后台执行)
```
docker-compose up --build
```
or 看系统安装的工具
```
docker compose up --build
```
会自动建立前后端与资料库<br>
前端port:3000<br>
后端port:3001<br>
资料库port:3306<br>

step 2
---
前端的一些套件需要手动安装 看警告缺什么装什么<br>
进入docker容器中的指令
```
docker exec -it container_name /bin/sh
```
容器名称使用以下指令查看，可输入代号的前三或前四位<br>
Ex: 容器代号为rfd9aewe2，则container_name 填入 rfd
```
docker ps -a
```
进入容器后输入
```
npm i package_name
```
需要安装以下这几个套件
```
/app # npm i @antv/l7 js-file-download dayjs @mui/x-date-pickers @antv/larkmap antd moment @ant-design/plots
```
step 3
---
需要手动在资料库汇入csv资料表：[下载地址](https://53znxn-my.sharepoint.com/:f:/g/personal/x_53znxn_onmicrosoft_com/El8qPtSv9npPuP2LoxVs9a0BUw6lxiTWzfC2aKSP3W7JMg?e=IcWGdL)<br>
四张资料表分别命名为epid vacc sex age<br>
也可以使用process.py中的程序插入资料，速度较快，但需要先手动汇入标题列<br>
登入帐户和密码为root<br>
