FROM apache:2.4-alpine
RUN apk update && apk upgrade && \
    apk add --update --no-cache \
      bash \
      git \
      openssh
ENV TZ Asia/Tokyo
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
ENV LANG C.UTF-8
WORKDIR /etc/www
COPY . .

EXPOSE 8080
