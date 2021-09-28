FROM maven:3-openjdk-8 as mvn
RUN git clone https://github.com/wakaleo/game-of-life.git && cd game-of-life && mvn package

FROM tomcat:8-jdk11-openjdk
LABEL Name="Tomcat"
COPY --from=mvn /game-of-life/gameoflife-web/target/gameoflife.war /usr/local/tomcat/webapps/gameoflife.war
EXPOSE 8080