FROM openjdk:8 AS BUILD_IMAGE
RUN apt update && apt install maven -y
#RUN git clone -b vp-docker https://github.com/imranvisualpath/vprofile-repo
#RUN cd vprofile-repo && mvn install
RUN git clone -b ci-jenkins https://github.com/tranqui89/vprofile-project
RUN cd ci-jenkins && mvn install

FROM tomcat:8-jre11

RUN rm -rf /usr/local/tomcat/webapps/*

COPY --from=BUILD_IMAGE vprofile-repo/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]