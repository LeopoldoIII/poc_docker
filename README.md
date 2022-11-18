# poc_docker
docker run

  `docker run 'image_name'`

  `docker run 'image_name:1.0'` specify image version
  
  `docker run -it image_name` to interact with the terminal 
  
  `docker run -p 80:5000 image_name` map port 80 = external port | 5000 = internal port
  
  `docker run -v /internal/vol:/container/vol image_name` to map container path in docker host 
  
info 
  
  `docker container ls -a` list all containers
  
  `docker inspect image_name` return info in json format
  
remove 
  
  `docker container rm container_id` to remove container by id, must be stoped 
  
  
# postgress

docker pull postgres:alpine

docker run --name postgres00 -e POSTGRES_PASSWORD=you_password -d -p 5432:5432 postgres:alpine

docker exec -it postgres00 bash


# selenium

docker run -d -p 4444:4444 --name selenium-hub -P selenium/hub:3.141.59

docker run -d -P --link selenium-hub:hub selenium/node-firefox-debug	

  
# Jenkins example 
``

# Jenkins ubuntu 

https://docs.docker.com/engine/install/ubuntu/

fix 
source https://adamtheautomator.com/docker-permission-denied/#:~:text=You've%20confirmed%20your%20Docker,group%20triggers%20permission%20denied%20error.

    docker: Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Post "http://%2Fvar%2Frun%2Fdocker.sock/v1.24/containers/create": dial unix /var/run/docker.sock: connect: permission denied.
    
    
    sudo groupadd docker
    
    sudo usermod -aG docker programmer
    
    sudo usermod -aG docker user
    
    sudo newgrp docker
    
    sudo chmod 666 /var/run/docker.sock

  
