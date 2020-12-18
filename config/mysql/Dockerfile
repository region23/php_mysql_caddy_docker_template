FROM mysql:5.7

ENV TZ=Europe/Moscow
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

COPY user.cnf /etc/mysql/mysql.conf.d/user.cnf
COPY init.sql /docker-entrypoint-initdb.d/
