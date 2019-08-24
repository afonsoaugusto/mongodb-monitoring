# mongodb-monitoring

Example data monitoring mongo db

```sh
sudo systemctl start docker
docker swarm init

docker stack deploy --prune -c docker-compose.yml stackdemo

docker stack services stackdemo
docker stack rm stackdemo


docker service ls
docker service ps --no-trunc cm0xlbx0cpmj

docker stop $(docker ps -a -q)
docker container rm $(docker container ls -aq)
docker volume rm $(docker volume ls -q)

```

```sh
curl -I 0.0.0.0:9000
HTTP/1.1 200 OK
Accept-Ranges: bytes
Cache-Control: max-age=31536000
Content-Length: 23032
Content-Type: text/html; charset=utf-8
Last-Modified: Fri, 26 Jul 2019 02:11:28 GMT
X-Content-Type-Options: nosniff
X-Xss-Protection: 1; mode=block
Date: Sat, 24 Aug 2019 01:15:13 GMT
```

## References

* [stefanprodan/swarmprom/docker-compose.yml](https://github.com/stefanprodan/swarmprom/blob/master/docker-compose.yml)
