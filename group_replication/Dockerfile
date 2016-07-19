FROM group_replication_base
MAINTAINER Daniël van Eeden <docker@myname.nl>

COPY my.cnf /etc/my.cnf
RUN /usr/sbin/mysqld --initialize-insecure --user=root
RUN chown -R mysql:mysql /var/lib/mysql
RUN chown mysql:mysql /var/log/mysqld.log
RUN sed -i 's/# user=mysql/user=mysql/' /etc/my.cnf

VOLUME /var/lib/mysql
EXPOSE 3306 33060
CMD ["mysqld"]
