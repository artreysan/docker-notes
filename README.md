# docker-notes

```
docker version
```

output:
```
Client:
 Version:           20.10.18
 API version:       1.41
 Go version:        go1.19.1
 Git commit:        b40c2f6b5d
 Built:             Sat Sep 10 11:31:10 2022
 OS/Arch:           linux/amd64
 Context:           default
 Experimental:      true

Server:
 Engine:
  Version:          20.10.18
  API version:      1.41 (minimum version 1.12)
  Go version:       go1.19.1
  Git commit:       e42327a6d3
  Built:            Sat Sep 10 11:30:17 2022
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          v1.6.8
  GitCommit:        9cd3357b7fd7218e4aec3eae239db1f68a5a6ec6.m
 runc:
  Version:          1.1.4
  GitCommit:
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0
```
## Search image in DockerHub
```
docker search <ImageName>
```

## Install image with the following command
```
docker pull <ImageName> 
```

## Watch the image download 
```
docker images
```
output:
```
REPOSITORY   TAG       IMAGE ID       CREATED       SIZE
ubuntu       latest    2dc39ba059dc   3 weeks ago   77.8MB
```
## Create container with image download  
```
docker run <ImageName>
```

## Delete the Image 
```
docker rmi <IMAGE ID>
```

# Containers

## Watch the container  
View corrently running containers
```
docker ps 
```
output:
```
CONTAINER ID   IMAGE     COMMAND   CREATED         STATUS         PORTS     NAMES
d163b4a58b4c   ubuntu    "bash"    5 minutes ago   Up 5 minutes             affectionate_mestorf
```
View corrently running containers and those that are no longer running
```
docker ps -a
```
output:
```
CONTAINER ID   IMAGE     COMMAND   CREATED          STATUS                       PORTS    NAMES
d163b4a58b4c   ubuntu    "bash"    17 minutes ago   Exited (130) 4 minutes ago            affectionate_mestorf
```

View only all CONTAINER ID 
```
doker ps -aq
```

## Delete container 
```
docker rm <NAME or CONTAINER ID>
```

## Delete all container with CONTAINER ID
```
docker rm $(docker ps -aq)
```

## Add external port (-p)
```
docker run -p <externalPort>:<internalPort> <ContainerName>
```
## Run container internally or background with detach (-d)
```
docker run -p <externalPort>:<internalPort> -d <ContainerName>
```









