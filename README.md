# DevOps_lab1 

> Made by Philonenko Igor, IK-01

--------------------------------------


## What you will need to build and run it locally:
 - [Docker](https://www.docker.com/)
 - [Node.js](https://nodejs.org)

--------------------------------------

## How to build docker image
1. Download source to your computer: ```git clone https://github.com/XimikBoda/DevOps_lab1.git```
2. Move into downloaded repo: ```cd DevOps_lab1/```
3. Build image: ```docker build . -t <image_name>```

Or you can get prebuild image from Docker Hub: ```docker pull ximikboda/myapp:latest```

--------------------------------------

## To push build image to docker hub:
1. Login into docker: ```docker login```
2. Push image to docker hub: ```docker push <image_name>:latest```

--------------------------------------

## How to run it locally
Run ```docker run -p 80:80 -m 128m --cpus="1" -d --name myapp --rm ximikboda/myapp```

### Some details about command above:
 - ```-p 80:80``` : Binds external port 80 to internal (inside container) port 80. 
 - ```-m 128m``` : Limits memory, which will be available to container. 
 - ```--cpus="1"``` : Specify how much of the available CPU resources a container can use.
 - ```-d``` : Run container in background.
 - ```--name myapp``` : Custom name for your docker container.
 - ```--rm``` : Remove container after stop.
 - ```ximikboda/myapp``` : Container name.

After that you can list all your running containers by running: ```docker ps```.

To stop container, run: ```docker stop myapp```