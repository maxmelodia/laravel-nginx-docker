# laravel-nginx-docker

<ul>
<li>docker network create laranet</li>

<li>docker build -t maxmelodia/laravel:prod . -f Dockerfile.prod</li>

<li>docker build -t maxmelodia/nginx:prod . -f Dockerfile.prod</li>

<li>docker run -d --network=laranet --name laravel maxmelodia/laravel:prod</li>

<li>docker run -d --network=laranet --name nginx -p 8080:80  maxmelodia/nginx:prod</li>
</ul>