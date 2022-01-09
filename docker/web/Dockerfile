FROM nginx:1.21.4-alpine

# timezoneをJSTにする
RUN apk --update-cache --no-cache add tzdata && \
    cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
    apk del --purge tzdata

COPY ./default.conf /etc/nginx/conf.d/default.conf
