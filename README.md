# Задание 1: 

docker pull mysql 
docker pull redis 

docker run -d \
  --name mysql \
  -e MYSQL_ROOT_PASSWORD=my-secret-pw \
  -e MYSQL_DATABASE=mydatabase \
  -e MYSQL_USER=myuser \
  -e MYSQL_PASSWORD=mypassword \
  -p 3355:3355 \
  --cpus="2.0" \
  --memory="1g" \
  --restart unless-stopped\
  -v my-volume:/var/lib/mysql \
  mysql:latest


docker run -d \
  --name redis \
  -p 6677:6677 \
  --cpus="2.0" \
  --memory="1g" \
  --restart unless-stopped\
  -v redis-volume:/data \
  redis:latest
  
  
docker restart mysql - рестарт mysql
docker restart redis - рестарт redis

docker stop mysql - останавливаем mysql
docker stop redis - останавливаем redis

docker rm mysql - удаляем mysql
docker rm redis - удаляем redis

# Задание 2:
docker-compose.yml
