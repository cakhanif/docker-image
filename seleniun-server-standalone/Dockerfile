FROM openjdk:11-jdk-slim

ENV SELENIUM_VERSION 4.0.0-alpha-2
ENV SELENIUM_VERSION_BASE 4.0

RUN apt-get update && apt-get -qq -y install curl \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/ \
    && rm -rf /tmp/downloaded_packages/ /tmp/*.rds

RUN curl -sSL https://selenium-release.storage.googleapis.com/${SELENIUM_VERSION_BASE}/selenium-server-standalone-${SELENIUM_VERSION}.jar -o /opt/selenium-server-standalone.jar

CMD ["java", "-jar", "/opt/selenium-server-standalone.jar"]