# PHM-SoftWare
一：项目环境部署
0.安装java
笔记本所使用的Java版本为1.8
1.	安装MYSQL server 和Nvicat
MYSQL版本为：Server version: 8.0.20
Mysql的安装和配置：https://www.cnblogs.com/fanghl/p/11400412.html
启动MYSQL server
打开Nvicat
此处没有设置全部变量，所以记得进入到/bin文件中运行
	net start mysql
	mysql -u root -p
	如果设置了密码就要输入密码 
2.	安装启动redis
使用版本为：3.2
	安装教程：https://www.jianshu.com/p/d324d5db6427
	进去redies的安装目录，打开cmd启动
	输入redis-server.exe redis.windows.conf命令
3.	node安装
使用版本为：版本号：v12.15
可使用命令判断版本号：node-v
4.	maven版本
使用版本为：3.6.3
进入bin文件夹。利用命令：mvn -v
5.用idea打开项目的pom.xml
	不同idea自带的Java，需要另外设置java版本设定java版本
https://www.cnblogs.com/yanwuliu/p/11134009.html
	不用idea自带的maven版本——https://www.jianshu.com/p/510368e05b3e
6.用vscode打开rouyi_ui
——下载相关npm包（安装相关依赖）
//从淘宝镜像下载 npm install --registry=https://registry.npm.taobao.org
启动命令——npm run dev
7.RabbitMQ安装配置（可以不安装）
——首先安装relang
https://blog.csdn.net/qq_47588845/article/details/107986373?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromBaidu-2.control&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromBaidu-2.control
——安装RabbitMQ
cd 进 sbin文件中输入命令启动
rabbitmq-plugins enable rabbitmq_management
8.python _flask后端环境部署
	利用anaconda安装flask虚拟环境，pyhton=3.6
	pycham选择flask虚拟环境中的python.exe
9.项目启动
在idea中点击RuoYi-adamin中的ruoyi-application启动项目
flask启动出现问题：
//Hdf5b版本不匹配   UserWarning: h5py is running against HDF5 1.10.5  when it was built against 1.10.4, this may cause problems   '{0}.{1}.{2}'.format(*version.hdf5_built_version_tuple)   //解决方法：卸载h5py后再安装   pip uninstall h5py   conda install h5py
9.连接时序数据库(https://www.cnblogs.com/yybrhr/p/11128149.html)
	公网ip:8.140.127.25
	cd /opt/soft/hadoop/opentsdb-2.4.0/build
时序数据库启动命令：（注意启动顺序不能出错）
//启动hadoop 
cd /opt/soft/hadoop/hadoop-3.1.2/ 
start-all.sh //同时将dfs和yarn集群启动)
 stop-all.sh
 //启动zookeeper 
zkServer.sh start 
zkServer.sh stop 
//安装
hbase start-hbase.sh 
//关闭
hbase stop-hbase.sh 
//启动opentsdb 
cd /opt/soft/hadoop/opentsdb-2.4.0/build //
启动命令：sh tsdb tsd &
正常运行后的进程：如果不是当前进程，则进程出错
 
10.git上传步骤
git add . 
git commit -m"备注" 
git push origin
三：Maven基本了解
1.查看maven版本
进入安装路径中
mvn-v或mvn-version
此处安装的版本的是3.6.3
2.不用maven中的mvn版本
在idea中集成Maven
https://blog.csdn.net/qq_40961980/article/details/86236498
