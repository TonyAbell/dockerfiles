FROM tonyabell/oracle-jdk

MAINTAINER Tony Abell<tabell@csod.com>

ENV ACTIVATOR_VERSION 1.2.12

RUN yum update -y && yum install -y unzip
RUN curl -O http://downloads.typesafe.com/typesafe-activator/$ACTIVATOR_VERSION/typesafe-activator-$ACTIVATOR_VERSION.zip
RUN unzip typesafe-activator-$ACTIVATOR_VERSION.zip -d / && rm typesafe-activator-$ACTIVATOR_VERSION.zip && chmod a+x /activator-$ACTIVATOR_VERSION/activator
ENV PATH $PATH:/activator-$ACTIVATOR_VERSION

EXPOSE 9000
RUN mkdir /app
WORKDIR /app
CMD ["activator", "run"]
