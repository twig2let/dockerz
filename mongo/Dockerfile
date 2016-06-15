FROM ubuntu:trusty

MAINTAINER Twig2let

# link mongo package
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv EA312927; \
    echo "deb http://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list;

# install base dependencies
RUN apt-get update && apt-get install -y -q; \
    apt-get install -y mongodb-org; \
    mkdir -p /data/db;

EXPOSE 27017
CMD ["service mongod start"]