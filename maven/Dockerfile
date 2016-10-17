FROM alpine:latest
MAINTAINER "Lee Faus <leefaus@gmail.com>"

RUN apk add --no-cache git bash openjdk8 wget

RUN wget http://www-us.apache.org/dist/maven/maven-3/3.3.9/binaries/apache-maven-3.3.9-bin.tar.gz
RUN tar -zxvf apache-maven-3.3.9-bin.tar.gz
RUN rm apache-maven-3.3.9-bin.tar.gz
RUN mv apache-maven-3.3.9 /usr/lib/apache-maven-3.3.9

ENV JAVA_HOME /usr/lib/jvm/java-1.8-openjdk
ENV JAVA=$JAVA_HOME/bin
ENV M2_HOME=/usr/lib/apache-maven-3.3.9
ENV M2=$M2_HOME/bin
ENV PATH $PATH:$JAVA_HOME:$JAVA:$M2_HOME:$M2
