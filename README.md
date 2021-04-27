# laravel-nginx-docker


docker network create laranet

docker build -t maxmelodia/laravel:prod . -f Dockerfile.prod
docker build -t maxmelodia/nginx:prod . -f Dockerfile.prod

docker run -d --network=laranet --name laravel maxmelodia/laravel:prod
docker run -d --network=laranet --name nginx -p 8080:80  maxmelodia/nginx:prod