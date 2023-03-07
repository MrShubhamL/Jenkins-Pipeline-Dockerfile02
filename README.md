# Jenkins-Pipeline-Dockerfile02
This is Docker file example 2

    FROM ubuntu
    MAINTAINER shubhamlohar55
    RUN apt update -y
    RUN apt install nginx -y
    WORKDIR /var/www/html
    ADD https://www.free-css.com/assets/files/free-css-templates/download/page288/global.zip .
    RUN apt update -y
    RUN apt install -y unzip
    RUN unzip global.zip
    RUN cp -rvf global-master/* .
    RUN rm -rf global-master global.zip
    CMD ["nginx", "-g", "daemon off;"]
    EXPOSE 80
