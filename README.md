# devOps-demo-project

##### How to varify docker version 
> docker --version

##### Varify Docker in your system
> docker ps
> docker ps --format=$FORMAT

##### What is Docker Image?
> An image is a read-only template with instructions for creating a Docker container. 
> Image is a template for creating an environment of your Choice. 
> Snapshot
> Has everything need to run your Apps
> OS, Software, Apss Code

##### What is Docker Container?
> A container is a runnable instance of an image. You can create, start, stop, move, or delete a container using the Docker API or CLI. You can connect a container to one or more networks, attach storage to it, or even create a new image based on its current state.

##### Pull docker image from docker registry 
> docker pull (ImageName)

##### run docker container 
> docker run ImageName
> docker run ImageName:latest (with Tag)

##### run docker container in detach mode
> docker run -d ImageName

##### run docker container in detach mode with port
> docker run -d - p 8080:80 ImageName


##### run docker container in detach mode with port and name
> docker run --name myDockerApp -d - p 8080:80 ImageName

##### run docker container 
> docker run --name mycontainer -d 

##### Start container
> docker container start 988c82a903f7

##### Start container
> docker container stop 988c82a903f7

##### How to use volume (mounted)
> docker run --name app -v /some/content:/usr/share/nginx/html:ro  -d -p 8080:80 nginx
> docker run --name app -v &(pwd):/usr/share/nginx/html:ro  -d -p 8080:80 nginx 
> docker run --name app -v &(pwd):/usr/share/nginx/html  -d -p 8080:80 nginx  (without read-only)

##### How to share volume (mounted)
> docker run --name app-copy --volumes-from website -d -p 8080:81 nginx
> docker run --name app -v &(pwd):/usr/share/nginx/html:ro  -d -p 8080:80 nginx 
> docker run --name app -v &(pwd):/usr/share/nginx/html  -d -p 8080:80 nginx  (without read-only)

##### How to go inside of conttainer
> docker exec -it myapp bash

##### This command witll restart application after start of docker desktop. 
> docker run - p 5000:5000 -d --restart=always imageName

##### Run mysql database for spring boot application
> docker run -p 8082:8081 --name my-springboot-appss --link mysql-standalone1:mysql -d customer-management

##### Run spring boot app
docker run --name mysql-standalone -d -e MYSQL_ROOT_PASSWORD=rootroot -e MYSQL_DATABASE=employee_directory -e MYSQL_USER=root -e MYSQL_PASSWORD=rootroot mysql:5.7


##### How to delete container
> docker container rm 988c82a903f7

##### This will remove all stopped containers.
> docker container prune

##### How build image from Dockerfile. 
> docker build Dockerfile
> docker build --tag myImage:latest .

##### How do versioning/tags/tagging for docker image 
> docker pull node:alpine
> docker pull node:latest

##### How do tagging change for docker image 
> docker tag nginx:latest xginx:1.01
>

##### How do inspect for docker container
> docker inspect ContainerNmae

##### How do inspect for docker container
> docker logs ContainerNmae
> docker logs -f ContainerNmae

##### How do exect for docker container
> docker exect -it ContainerName bash
> docker exect -it ContainerName sh


##### How to see system info. 
> docker system df

##### How see even. 
> docker events

##### How see top. 
> docker top containerName




