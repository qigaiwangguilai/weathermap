FROM openjdk:8u181-jdk-alpine

RUN sleep 6000

RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone

RUN echo "Current directory: $(pwd)"

WORKDIR /home/apps/

RUN echo "Current2 directory: $(pwd)"

ADD target/forecast-1.0.0.jar .
ADD start.sh .

ENTRYPOINT ["sh", "/home/apps/start.sh"]
