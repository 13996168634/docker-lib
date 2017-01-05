FROM    docker.io/alvintz/centos:7.2.1511
MAINTAINER    Alvin  tz466731927@126.com
RUN	yum -y install initscripts redhat-lsb-core
ADD	td-agent-2.3.3-0.el7.x86_64.rpm /root/
RUN rpm -ivh /root/td-agent-2.3.3-0.el7.x86_64.rpm && rm -f /root/td-agent-2.3.3-0.el7.x86_64.rpm
RUN	/usr/sbin/td-agent-gem install fluent-plugin-elasticsearch fluent-plugin-typecast fluent-plugin-secure-forward
ENTRYPOINT	["/etc/init.d/td-agent" , "start"]