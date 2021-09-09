# devOps-demo-project

> Pull docker image from docker registry 
docker pull (ImageName)

> Run mysql database for spring boot application
docker run -p 8082:8081 --name my-springboot-appss --link mysql-standalone1:mysql -d customer-management

> Run spring boot app
docker run --name mysql-standalone -e MY_SQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=employee_directory -e MYSQL_USER=root -e MYSQL_PASSWORD=rootroot -d mysql:5.6

> Start container
ocker container start 988c82a903f7

> This will remove all stopped containers.
docker container prune

> This command witll restart application after start of docker desktop. 
docker run - p 5000:5000 -d --restart=always imageName
