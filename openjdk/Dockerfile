FROM alpine:latest

RUN apk add --no-cache git curl ca-certificates && rm -rf /var/cache/apk/*
RUN mkdir -p /opt/adoptopenjdk
RUN curl -X GET -L -o /tmp/adoptopenjdk.tar.gz https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_x64_alpine-linux_hotspot_16.0.1_9.tar.gz
RUN tar -xvf /tmp/adoptopenjdk.tar.gz -C /opt/adoptopenjdk
RUN rm /tmp/adoptopenjdk.tar.gz
ENV JAVA_HOME="/opt/adoptopenjdk/jdk-16.0.1+9" \
    PATH="/opt/adoptopenjdk/jdk-16.0.1+9/bin:$PATH"

CMD [ "jshell" ]
