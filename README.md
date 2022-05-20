## Please reading the note in each file

## Install Docker & Docker Compose first

#### Docker
```html
https://docs.docker.com/get-docker/
```

#### Docker Compose
```html
https://docs.docker.com/compose/install/
```





## Development/Deploy with Docker Compose

#### Must be created an external network named: `traefik-public`

```html
docker network create traefik-public
```

#### Build

```html
docker-compose build OR docker-compose build -f custom-filename.yml
```

#### Run compose

```html
Note: If you want to run separate files, the flow will be : db => proxy+wordpress => phpmyadmin[optional]
```

```html
docker-compose up OR docker-compose up -d
```

```html
docker-compose -f custom-filename.yml up OR docker-compose custom-filename.yml up -d
```





## Others

#### Check list networks

```html
docker network ls
```

#### Removes one of networks

```html
docker network rm NETWORK_NAME/NETWORK_ID
```

#### Check list containers

```html
docker ps OR docker-compose ps
```

#### Stop one of containers

```html
docker stop CONTAINER_ID/CONTAINER_NAME OR docker-compose stop CONTAINER_ID/CONTAINER_NAME
```

#### Stop all containers

```html
docker stop $(docker ps -a -q) OR docker-compose stop
```

#### Check list volumes

```html
docker volume ls
```

#### Remove one of volumes

```html
docker volume rm VOLUME_ID
```

#### Remove all volumes

```html
docker volume rm $(docker volume ls)
```

#### Remove unused data

```html
docker system prune -f
```

#### If you are got an error, follow bellow step...

```html
https://gist.github.com/eloypnd/5efc3b590e7c738630fdcf0c10b68072
```
