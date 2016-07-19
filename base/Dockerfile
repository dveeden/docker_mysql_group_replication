FROM centos:centos7
MAINTAINER Daniël van Eeden <docker@myname.nl>

ADD http://downloads.mysql.com/snapshots/pb/mysql-group-replication-0.7.0-labs/mysql-group-replication-0.7.0-labs-linux-el7-x86-64bit.tar.gz /build/
ADD http://downloads.mysql.com/archives/get/file/mysql-community-client-5.7.10-1.el7.x86_64.rpm /build/
ADD http://downloads.mysql.com/archives/get/file/mysql-community-common-5.7.10-1.el7.x86_64.rpm /build/
ADD http://downloads.mysql.com/archives/get/file/mysql-community-server-5.7.10-1.el7.x86_64.rpm /build/
ADD http://downloads.mysql.com/archives/get/file/mysql-community-libs-5.7.10-1.el7.x86_64.rpm /build/
RUN yum -y localinstall /build/*rpm
RUN tar xf /build/mysql-group-replication-0.7.0-labs-linux-el7-x86-64bit.tar.gz -C / --strip-components 1 --keep-old-files
