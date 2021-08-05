FROM ubuntu:18.04 
RUN apt-get update
RUN apt-get install curl -y
RUN curl -sl https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install nodejs -y
WORKDIR /opt/node-app
COPY . /opt/node-app/
ENV channel=kanaladi
CMD ["node","index.js"];


