FROM ubuntu:16.04

COPY ./entrypoints /entrypoints

WORKDIR /opt/server

RUN apt-get update && apt-get install -y build-essential curl git make
RUN curl -sL https://deb.nodesource.com/setup_6.x | bash -
RUN apt-get update && apt-get install -y nodejs && npm install -g npm@5.6
RUN mkdir node_modules
RUN chmod -R 777 node_modules
ENV PATH="/opt/server/node_modules/.bin:${PATH}"

CMD /entrypoints/run
