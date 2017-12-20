# filebeat-alpine
filebeat with alpine, more tiny, more lighter

# Make sure your application log path need to follow below or link to below path.
```
PATH/applition/logs/*.log
```

# And change [docker-compose file](https://github.com/easonlau02/filebeat-alpine/blob/master/docker-compose.yml)
```
volumes:
  - PATH:/home/user/ 
```

# Run via docker-compose
```
docker-compose up -d
```

# docker ps | grep filebeat-alpine
```
CONTAINER ID        IMAGE                           COMMAND                  CREATED             STATUS              PORTS               NAMES
8b7a1d8a35c0        eason02/filebeat-alpine:5.3.1   "filebeat -e filebeat"   18 seconds ago      Up 17 seconds                           filebeat-alpine-5.3.1
```



