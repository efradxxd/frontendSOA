FROM ubuntu
RUN apt-get -y update \
    && apt-get -y upgrade \
    && apt-get install -y apache2 \
    && apt-get install nano \
    && chown -R mysql:mysql /var/lib/mysql /var/run/mysqld \
    && apt-get -y install mysql-server \
    && apt-get install -y nodejs npm git\
    && rm /var/www/html/index.html \
    && cd var/www/html \
    && git clone https://github.com/efradxxd/productionSOA.git \
    && mv productionSOA/dist/* . \
    && cd / && mkdir backend && cd backend \
    && service apache2 start \


    COPY ./* /var/www/html

EXPOSE 80
EXPOSE 3000
EXPOSE 3306