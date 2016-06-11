# dockerz
Collection of Dockerfiles.

### Usage

1. Copy the Dockerfile to the root of your project
2. Run the following from the project root directory:
```sh
docker build -t {MY_IMAGE_NAME} .
```

### dev/Dockerfile
Builds a very bare-bones image, good starting point for nodeJS application development.  

Creates an Ubuntu:14.04 image and installs:

* cURL
* [NVM](https://github.com/creationix/nvm#install-script)
* NPM *latest*
* NodeJS *v4.4.5*

