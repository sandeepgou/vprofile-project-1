FROM maven:3.9-eclipse-temurin-17 AS build

RUN git clone https://github.com/sandeepgou/vprofile-project-1.git
RUN cd vprofile-project-1 && git checkout containers && mvn install

FROM tomcat:10.1-jdk17-temurin
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=build vprofile-project-1/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080

CMD ["catalina.sh", "run"]
