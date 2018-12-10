FROM tomcat:7.0
MAINTAINER praveen
ADD https://downloads.sourceforge.net/project/openmrs/releases/OpenMRS_Platform_2.0.4.1/openmrs.war /usr/local/tomcat/webappas/openmrs.war
EXPOSE 8080
CMD ["catalina.sh", "run"]


# Httpd on Ubuntu 
FROM ubuntu:15.04
MAINTAINER Praveen Bhavikatti
RUN apt-get update && apt-get install httpd && apt-get clean \
    rm -rf /tmp/*
CMD ["/bin/bash"] 

#httpd On Centos/Redhat
FROM centos:7
MAINTAINER praveen
RUN yum install httpd -y 
    rm -rf /tmp/*
CMD ["/bin/bash"] 


#Deploying War file into container any OS

FROM tomcat:7
ADD  https://updates.jenkins-ci.org/download/war/2.150/jenkins.war /usr/local/tomcat/webapps/jenkins.war
EXPOSE 8080
USER praveen
#RUN service tomcat7 restart
CMD ["bin/catalina.sh","run"]