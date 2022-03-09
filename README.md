# docker-image
常用的docker镜像  

镜像制作基本流程:  
[dockerfile编写规则](https://docs.docker.com/engine/reference/builder/)  
```shell
# 创建文件  
touch Dockerfile

# 编写 Dockerfile
FROM centos:7.9.2009
...

# 构建 -t tag -f file
docker build -t tag .

# 上传镜像
sudo docker push 

```
- ### [FTP服务](https://github.com/delfer/docker-alpine-ftp-server)  
- ### [Telnet服务](telnet-server/README.md)    
