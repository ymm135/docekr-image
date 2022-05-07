# Telnet服务 

```
# 下载镜像
docker pull centos

# 启动镜像
docker run -d -p 5000:23 --name centos7 --privileged=true centos /usr/sbin/init

# 进入镜像
docker exec -it centos7 /bin/bash

# 安装
yum install net-tools telnet-server telnet xinetd 

# 开机启动
systemctl enable xinetd.service 
systemctl enable telnet.socket 

# 启动服务
systemctl start telnet.socket
systemctl start xinetd

# 创建用户
adduser test
passwd test

# 宿主机测试
$ telnet localhost 5000

```

telnet配置: 
```shell
systemctl status telnet.socket
```


