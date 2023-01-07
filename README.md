# node_file_server
Node + Express file services

用来申请https证书的时进行文件验证用的

public/ 目录下是对应的文件
默认是 http 协议，80端口

# 运行
npm start

在windows上报错: Port 80 requires elevated privileges
大概率是启用了iis服务。在 services.msc 中停用 World Wide Web Publishing Service 即可

在linux上报这个错，是因为非 root 用户不能使用 1024 一下的端口
此时使用 sudo npm start 和 sudo pm2 start 都会报错。要使用如下命令:
sudo node ./bin/www 才可以