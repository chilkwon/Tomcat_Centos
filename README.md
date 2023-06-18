# Tomcat_Centos

FROM centos:7
RUN yum install java -y
RUN mkdir /opt/tomcat
WORKDIR /opt/tomcat
ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.76/bin/apache-tomcat-9.0.76.tar.gz .
RUN tar -xvzf apache-tomcat-9.0.76.tar.gz
RUN mv apache-tomcat-9.0.76/*  /opt/tomcat
EXPOSE 8080
CMD ["/opt/tomcat/bin/catalina.sh","run"]


# Pull centos from dockerhub
# Install java
# Create/opt/tomcat directory
# Change work directory to /opt/tomcat
# Downlod tomcat packages
# Extract tar.gz file
# Rename to tomcat directory
# Tell to docker that it runs on port 8080
# Start tomcat services
