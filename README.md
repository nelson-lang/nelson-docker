# nelson-docker

Docker official image for Nelson.

See the Docker Hub page for the full readme on how to use this Docker image and for information regarding contributing and issues.

snap with graphical interface can be installed with:
```bash
sudo snap install nelson
```

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

## Release on dockerhub

```bash
docker rmi $(docker images -q) -f
docker system prune -a

export NELSON_VERSION=1.6.0
docker build -t nelsonsoftware/nelson:latest -t nelsonsoftware/nelson:v$NELSON_VERSION .
docker push  nelsonsoftware/nelson:vNELSON_VERSION
docker push  nelsonsoftware/nelson:latest

```
