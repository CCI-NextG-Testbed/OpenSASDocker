# OpenSASDocker
Docker file to create a image for OpenSAS core and dashboard

## Building  the image
Docker Engine needs to be installed to proceed further

Clone the OpenSASDocker repository and run cd OpenSASDocker (go into clone directory)

Next run the docker build command:
sudo docker build . --tag=opensas-server-dash --no-cache

The docker build process starts and will take a few minutes. A image named opensas-server-dash will be created.

## Running the container using the created image

To start OpenSAS simply run:
docker run --network=host --name=opensas-container -it --privileged opensas-server-dash

This start the two services
1) The OpenSAS core which will listen to HTTP requests from CBSDs
2) The OpenSAS dashboard webserver

## Using OpenSAS

The web portal can be access via http://localhost:9528/

The CBSDs can access the SAS via the following URL endpoints:

http://localhost:1443/sas-api/registration

http://localhost:1443/sas-api/spectrumInquiry

http://localhost:1443/sas-api/grant

http://localhost:1443/sas-api/heartbeat

http://localhost:1443/sas-api/relinquishment

http://localhost:1443/sas-api/deregistration

