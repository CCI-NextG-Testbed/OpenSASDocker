# OpenSASDocker
Docker file to create a image for OpenSAS core and dashboard

## Building  the container
Docker Engine needs to be installed to proceed further

Clone the OpenSASDocker repository and run cd OpenSASDocker

Next run the docker build command:
sudo docker build . --tag=opensas-server-dash --no-cache

The docker build process starts and will take a few minutes. A image named opensas-server-dash will be created.

To start OpenSAS simply run:
docker run --network=host -it --privileged opensas-server-dash

This start the two services
1) The OpenSAS core which will listen to HTTP requests from CBSDs
2) The OpenSAS dashboard webserver
