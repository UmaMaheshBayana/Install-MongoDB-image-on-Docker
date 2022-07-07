
# Install MongoDB in Docker
 
 ```
 docker container run -d --restart unless-stopped -p 27018:27017 --name mongodb -e  MONGO_INITDB_ROOT_USERNAME=sanela -e MONGO_INITDB_ROOT_PASSWORD=san3la mongo:latest
```

# MongoDB docker container Backup
```docker exec CONTAINER_ID sh -c 'exec mongodump -u sanela -p san3la --gzip --archive' > FILENAME.gz```

# MongoDB Docker container restore

```docker exec -i container_ID sh -c 'mongorestore --authenticationDatabase admin -u sanela -p san3la --gzip --archive' < file.gz```
