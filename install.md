# Koha 安裝
## 使用 Docker
* [Koha-docker Wiki](https://github.com/digibib/koha-docker/wiki/Using-the-Koha-Docker-image)  
* [Docker 安裝 MariaDB](https://mariadb.com/resources/blog/mariadb-and-docker-use-cases-part-1/)  
* [Docker Volumes](https://docs.docker.com/storage/volumes/)
* [Docker 容器互連](https://philipzheng.gitbooks.io/docker_practice/content/network/linking.html)

## Docker Compose
下載 [Koha-docker](https://github.com/digibib/koha-docker)，`cd docker-compose`。  
編輯 `build.yml`、`docker-compose.env` 、`build.yml`，參考[ENV](https://github.com/digibib/koha-docker/wiki/Environment-and-Configuration)  
設定 common.yml:
```
image: "digibib/koha:latest"
```
```
$ source docker-compose.env && sudo docker-compose -f build.yml -f common.yml up -d
```  
