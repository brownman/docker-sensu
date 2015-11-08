FROM centos
MAINTAINER sverrest@gmail.com

COPY sensu.repo /etc/yum.repos.d/sensu.repo

RUN yum -y install sensu && \
    rpm -Uvh http://dl.bintray.com/palourde/uchiwa/uchiwa-0.12.1-1.x86_64.rpm

COPY config.json /etc/sensu/config.json
COPY uchiwa.json /etc/sensu/uchiwa.json

EXPOSE 4567

CMD /bin/bash
