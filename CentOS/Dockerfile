FROM centos:6.6

MAINTAINER Nandaja Varma <nandaja.varma@gmail.com>
RUN yum --setopt=tsflags=nodocs -y install wget openssh
RUN wget http://download.gluster.org/pub/gluster/glusterfs/3.6/3.6.2/CentOS/glusterfs-epel.repo -O /etc/yum.repos.d/glusterfs-epel.repo
RUN yum --setopt=tsflags=nodocs -y install glusterfs glusterfs-server glusterfs-fuse glusterfs-geo-replication glusterfs-cli glusterfs-api
RUN yum clean all

RUN echo 'root:password' | chpasswd
ADD start-gluster.sh /

CMD /bin/sh start-gluster.sh

EXPOSE 22 111 245 443 24007 2049 8080 6010 6011 6012 38465 38466 38468 38469 49152 49153 49154 49156 49157 49158 49159 49160 49161 49162
