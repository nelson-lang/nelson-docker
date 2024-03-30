# nelson-docker

Docker official image for Nelson.

See the Docker Hub page for the full readme on how to use this Docker image and for information regarding contributing and issues.

## build docker

```bash
docker build -t nelson .
```

## download nelson image

```bash
docker pull nelsonsoftware/nelson
```

## run docker

```bash
docker run -ti nelsonsoftware/nelson
```

With graphical user interface:

```bash
docker run -it --env="DISPLAY" --env="QT_X11_NO_MITSHM=1" --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" --entrypoint /nelson/bin/linux/nelson-gui nelsonsoftware/nelson
```

## Release on dockerhub

```bash
docker rmi $(docker images -q) -f
docker system prune -a

docker build -t nelsonsoftware/nelson:latest -t nelsonsoftware/nelson:v1.3.0 .
docker push  nelsonsoftware/nelson:v1.3.0
docker push  nelsonsoftware/nelson:latest

```
