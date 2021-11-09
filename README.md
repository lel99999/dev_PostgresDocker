# dev_PostgresDocker
Postgresql Testing with Containers

#### On Macs, install Postgresql Client (libpq)
- [https://content-www.enterprisedb.com/downloads/postgres-postgresql-downloads](https://content-www.enterprisedb.com/downloads/postgres-postgresql-downloads) <br/>

- libpq

```
$brew install libpq
```

#### Build Multiple Images with Dockerfile
- [https://docs.docker.com/engine/reference/commandline/build/#specifying-target-build-stage---target](https://docs.docker.com/engine/reference/commandline/build/#specifying-target-build-stage---target) <br/>

```
$docker build -t image1 --target img1 .
```


#### Build Multiple Images with docker-compose
- add target: <br/>
```
version: '3.4'
services:
  img1:
    build:
      context: .
      target: img1
  img2:
    build:
      context: .
      target: img2
```
