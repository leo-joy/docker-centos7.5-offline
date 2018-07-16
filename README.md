#docker在centos7.5下离线安装

#已上传了8个依赖包，还有两个包可以到网站上自己下载

#下载链接：container-selinux-2.9-4.el7.noarch.rpm
ftp://mirror.switch.ch/pool/4/mirror/scientificlinux/7x/external_products/extras/x86_64/container-selinux-2.9-4.el7.noarch.rpm

#下载链接：docker-ce-17.12.0.ce-1.el7.centos.x86_64.rpm
https://download.docker.com/linux/centos/7/x86_64/stable/Packages/docker-ce-17.12.0.ce-1.el7.centos.x86_64.rpm

#然后把上面的两个包放在rpm目录中

#在把这个安装包中8个依赖包也下载下来，放在docker文件夹中，把上面的rpm文件也放在这个docker文件夹中；

#可以把docker文件夹打成一个zip包，拷贝的离线的linux主机上，用root权限执行install.sh这个脚本；

#离线安装docker

cp -r docker.zip /home
cd /home
unzip docker.zip

rpm -ivh /home/docker/*.rpm

rpm -ivh /home/docker/rpm/container-selinux-2.9-4.el7.noarch.rpm

rpm -ivh/home/docker/rpm/docker-ce-17.12.0.ce-1.el7.centos.x86_64.rpm

service docker start

docker -v
