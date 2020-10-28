# poc_docker
docker run

  `docker run 'image_name'`

  `docker run 'image_name:1.0'` specify image version
  
  `docker run -it image_name` to interact with the terminal 
  
  `docker run -p 80:5000 image_name` map port 80 = external port | 5000 = internal port
  
  `docker run -v /internal/vol:/container/vol image_name` to map container path in docker host 
  
info 
  
  `docker inspect image_name` return info in json format

