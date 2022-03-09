FROM centos:7.9.2009
MAINTAINER Docker xiaoming <at.xiao.ming.cn@gmail.com> 
RUN yum install net-tools -y
RUN yum install telnet-server -y
RUN yum install telnet -y
RUN yum install xinetd -y

RUN echo "root:root" | chpasswd

RUN mkdir /data
RUN echo -e '#!/bin/bash ' > /data/start.sh
RUN echo -e 'systemctl start telnet.socket' >> /data/start.sh
RUN echo -e 'systemctl start xinetd' >> /data/start.sh
RUN chmod +x /data/start.sh

ENTRYPOINT ["/data/start.sh"] 



