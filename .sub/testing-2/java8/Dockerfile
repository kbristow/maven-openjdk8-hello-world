FROM harbor.bison.sdc-prod.caas.absa.co.za/bison-cloud/sub-openjdk8-jre:latest

RUN mkdir -p /usr/src/app

COPY target/*.jar /usr/src/app
RUN mv `ls /usr/src/app/*.jar | head -n 1` /usr/src/app/app.jar

EXPOSE 8080
ENTRYPOINT ["java","-jar","/usr/src/app/app.jar"]
