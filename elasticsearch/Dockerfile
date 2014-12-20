FROM tonyabell/oracle-jdk

MAINTAINER Tony Abell<tabell@csod.com>

ENV ES_PKG_NAME elasticsearch-1.4.1
RUN yum -y install tar
RUN cd / && wget https://download.elasticsearch.org/elasticsearch/elasticsearch/$ES_PKG_NAME.tar.gz
RUN tar xvzf $ES_PKG_NAME.tar.gz && rm -f $ES_PKG_NAME.tar.gz && mv /$ES_PKG_NAME /elasticsearch
VOLUME ["/data"]
WORKDIR /data
CMD ["/elasticsearch/bin/elasticsearch"]
EXPOSE 9200
EXPOSE 9300
