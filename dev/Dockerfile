FROM ubuntu:trusty

MAINTAINER Twig2let

# install base dependencies
RUN apt-get update && apt-get install -y -q \	
	curl;

ENV NVM_DIR 	   /usr/local/nvm
ENV NODE_VERSION   4.4.5

RUN curl https://raw.githubusercontent.com/creationix/nvm/v0.24.1/install.sh | sh;

# invoke nvm to install node
RUN cp -f $NVM_DIR/nvm.sh $NVM_DIR/nvm-tmp.sh; \
	echo "nvm install $NODE_VERSION; nvm alias default $NODE_VERSION" >> $NVM_DIR/nvm-tmp.sh; \
  	sh $NVM_DIR/nvm-tmp.sh; \
   	rm $NVM_DIR/nvm-tmp.sh;

# update to latest npm
RUN $NVM_DIR/versions/node/v$NODE_VERSION/bin/npm i npm -g

ENV NODE_PATH $NVM_DIR/v$NODE_VERSION/lib/node_modules
ENV PATH      $NVM_DIR/v$NODE_VERSION/bin:$PATH

EXPOSE 80