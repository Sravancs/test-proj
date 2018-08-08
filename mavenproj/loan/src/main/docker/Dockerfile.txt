FROM dockerfile/java:oracle-java8

VOLUME /tmp
ADD loan.jar /opt/loan/
EXPOSE 8080
WORKDIR /opt/loan/
CMD ["java", "-Djava.security.egd=file:/dev/./urandom", "-Xms512m", "-Xmx1g", "-jar", "loan.jar"]
