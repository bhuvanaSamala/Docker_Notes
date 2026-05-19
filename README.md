

**# Docker_Notes**


**

BASIC COMMANDS**
Docker ps --> shows the running containers.
Docker ps -a --> shows running, stopped containers.
Docker images --> shows the list of images in docker.
Docker start <container ID> --> starts that container.
Docker stop <container ID> --> stops that container.
Docker rm --> delete container.
Docker rmi --> delete the image.
docker logs <container ID> --> checks the logs of containers.
Docker inspect <containerID> --> details of container.
Docker restart <container ID> --> restarts the container.



**IMAGES :**
List all Local images
docker images
Delete an image
docker rmi <image_name>
Remove unused images
docker image prune
Build an image from a Dockerfile
docker build -t <image_name>:<version> . //version is optional
docker build -t <image_name>:<version> . -no-cache //build without cache

**
CONTAINER :**
List all Local containers (running & stopped)
docker ps -a
List all running containers
docker ps
Create & run a new container
docker run <image_name>
//if image not available locally, it’ll be downloaded from DockerHub
Run container in background
docker run -d <image_name>
Run container with custom name
docker run - -name <container_name> <image_name>
Port Binding in container
docker run -p<host_port>:<container_port> <image_name>
Set environment variables in a container
docker run -e <var_name>=<var_value> <container_name> (or <container_id)
Start or Stop an existing container
docker start|stop <container_name> (or <container_id)
Inspect a running container
docker inspect <container_name> (or <container_id)
Delete a container
docker rm <container_name> (or <container_id)




docker tag <imagename:version> <username/imagename:version>
docker push <username/imagename:version>
docker pause <containerid>
docker unpause <containerID> 
