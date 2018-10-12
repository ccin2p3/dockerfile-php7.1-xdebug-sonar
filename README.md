# PHP 7.1 cli with xdebug and sonar scanner

This image allows you to run and debug your PHP code and the ability to run sonar scanner on your project thanks to Docker.

Installation
---

### Pull from Docker Hub
```
docker pull ccin2p3/php7.1-xdebug-sonar
```

### Or build from GitHub
```
docker build -t ccin2p3/php7.1-xdebug-sonar github.com/ccin2p3/dockerfile-php7.1-xdebug-sonar
```

### Run image
```
docker run -it ccin2p3/php7.1-xdebug-sonar bash
```

### Or use as base image
```Dockerfile
FROM ccin2p3/php7.1-xdebug-sonar
```

### Or use it with docker-compose
```yml
app:
  image: ccin2p3/php7.1-xdebug-sonar
  ports:
    - 9000:9000
  expose:
    - 9000
  environment:
    PHP_XDEBUG_ENABLED: 1
  tty: true
  stdin_open: true
```
