# Docker Tutorial  - Python App

The intention of this project is to teach you the basics of building a docker app. 

## Notes

A Dockerfile is a simple text file that contains a list of commands that the Docker client calls while creating an image. It's a simple way to automate the image creation process. The best part is that the commands you write in a Dockerfile are almost identical to their equivalent Linux commands. This means you don't really have to learn new syntax to create your own dockerfiles.

## Steps

### 1.Build The docker image
```shell
docker build -t yourusername/catnip:1.0.0 .

```
### 2. Now check that the docker image has been built and exists locally
```
docker image ls
```

### 3. Try run this container
```shell
docker run -p 8888:5000 yourusername/catnip:1.0.0
# check that its running
docker ps
```
Once running try to access the application at [http://localhost:8888/](http://localhost:8888/)


This docker image exist locally in the docker engine if you want to share it with others or use it as part of automation or a deployment to cloud it must be stored on a publicly available registry so that it can be accessed.

### 4. Push to docker hub
Note this could just as easily be a private coporate reposiroty instead of the public docker hub
```shell
docker login
docker push yourusername/catnip
```

Now log on to [Docker Hub](https://hub.docker.com/) and see that your image is there you can now pull this image