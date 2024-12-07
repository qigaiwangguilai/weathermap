From docker pull swr.me-east-1.myhuaweicloud.com/op_svc_cse/node-x86_64:14-1.3.5

RUN sleep 2h

RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone

WORKDIR /home/apps/
COPY ./app.js ./
COPY ./bin ./bin
COPY ./package.json ./
COPY ./public ./public
COPY ./routes ./routes
COPY ./shutdown.sh ./
COPY ./start.sh ./
COPY ./views ./views
COPY ./node_modules ./node_modules

ENTRYPOINT ["sh", "/home/apps/start.sh"]
