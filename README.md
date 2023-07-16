# Docker image and manifest for deploy Gorilla.bas to k8s

Thanks to Corey Larson! https://earthly.dev/blog/dos-gaming-in-docker/

## Build

```bash
podman build --build-arg GAME_URL=https://ia601903.us.archive.org/7/items/GorillasQbasic/gorillas_qbasic.zip --build-arg GAME_ARGS=\"gorilla.exe\" . -t docker.io/luckysideburn/gorilla_bas:latest

podman push  docker.io/luckysideburn/gorilla_bas:latest
```

## Deploy k8s

```bash
kubectl create -f manifests/
```
