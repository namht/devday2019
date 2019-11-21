#######
# 
# How to build docker image: 
# sudo docker build  -t team3_devday_server:v1 .
#
# Start docker image:
# sudo docker run -d --name team3-devday-server-v1  -it -p 18080:18080 -v /usr/share/logs/data:/logs team3_devday_server:v1 
#######
FROM openjdk:11.0.4-jdk

USER root
run mkdir /opt/devday2019

ADD ./devday2019project-0.0.1-SNAPSHOT.jar /opt/devday2019
ADD ./group3_application.properties /opt/devday2019

run ls -l /opt/devday2019
EXPOSE 18080

# Set the default command to run on boot
# This will start Spring boot application by default on port 


ENTRYPOINT ["java", "-jar", "/opt/devday2019/devday2019project-0.0.1-SNAPSHOT.jar","--spring.config.location=/opt/devday2019/group3_application.properties"]



