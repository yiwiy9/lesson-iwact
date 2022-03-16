FROM node:16-alpine3.14

# timezoneをJSTにする
RUN apk --update-cache --no-cache add tzdata && \
    cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
    apk del --purge tzdata

WORKDIR /home/frontend
