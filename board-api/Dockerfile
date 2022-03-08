FROM openjdk:8-jdk-alpine
VOLUME /tmp
#ARG JAR_FILE=target/*.jar
ARG JAR_FILE= board-api/target/*.jar
COPY ${JAR_FILE} app.jar
EXPOSE 8090
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
