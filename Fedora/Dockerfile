FROM fedora:21

MAINTAINER Nandaja Varma <nandaja.varma@gmail.com>
RUN yum -y install wget deltarpm
RUN wget http://download.gluster.org/pub/gluster/glusterfs/3.6/3.6.2/Fedora/glusterfs-fedora.repo -O /etc/yum.repos.d/glusterfs-fedora.repo
RUN yum --setopt=tsflags=nodocs -y install glusterfs glusterfs-server glusterfs-fuse glusterfs-geo-replication glusterfs-cli glusterfs-api
RUN yum clean all

ADD start-gluster.sh /

CMD /bin/bash start-gluster.sh


EXPOSE 22 111 245 443 24007 2049 8080 6010 6011 6012 38465 38466 38468 38469 49152 49153 49154 49156 49157 49158 49159 49160 49161 49162
