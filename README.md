# docker-centos7.5-offline
docker在centos7.5下离线安装

#/bin/bash

#离线安装docker
cp -r docker.zip /home
cd /home
unzip docker.zip

rpm -ivh /home/docker/*.rpm

rpm -ivh /home/docker/rpm/container-selinux-2.9-4.el7.noarch.rpm

rpm -ivh/home/docker/rpm/docker-ce-17.12.0.ce-1.el7.centos.x86_64.rpm

service docker start

docker -v
