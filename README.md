# cbse12th

## Commands for starting docker images

Create network first
```
docker network create cbse
```

For starting mysql
```
docker run -d --name mysql-container --network=cbse -e MYSQL_ROOT_PASSWORD=test1234 -p 3306:3306 mysql:latest
```

For starting phpmyadmin
```
docker run --name phpmyadmin-container --network=cbse -e PMA_HOST=mysql-container -e PMA_PORT=3306 -p 8080:80 phpmyadmin/phpmyadmin:latest
```

For starting jupyter
```
 docker run  --network=cbse -p 8888:8888 -v notebooks:/home/jovyan/work jupyter/base-notebook

```