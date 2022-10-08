# FROM hum-app:1.0.0

# RUN mkdir /build

# WORKDIR /build

# COPY ./entrypoint.sh /build/entrypoint.sh

# COPY ./target/spring-boot-initial-0.0.1-SNAPSHOT.jar /build/service.jar

# EXPOSE 8080

# RUN chmod a+x /build/entrypoint.sh

# ENTRYPOINT [ "/build/entrypoint.sh" ]


FROM humana-dss:1.0.0 

#RUN apt update && add openjdk11

RUN mkdir /build

COPY ./target/spring-boot-initial-0.0.1-SNAPSHOT.jar /build/service.jar

COPY ./startup.sh /startup1.sh

EXPOSE 8080

RUN chmod a+x /startup1.sh

# CMD ["/startup1.sh"]

ENTRYPOINT [ "sh", "/startup1.sh" ]
