FROM amazonlinux

RUN yum -y update
RUN yum -y install httpd
RUN yum -y install php

COPY custom.conf /etc/httpd/conf.d/custom.conf
COPY ./index.php /var/www/html/index.php


CMD ["/bin/sh", "-c", "/usr/sbin/php-fpm && /usr/sbin/httpd -D FOREGROUND"]
#CMD ["/usr/sbin/httpd","-D","FOREGROUND"]

EXPOSE 80
