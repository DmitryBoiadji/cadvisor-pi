# cAdvisor Pi

cAdvisor docker image build for ARM devices (for example: Raspberry PI).  
This package is based on official [google/cadvisor](https://github.com/google/cadvisor).

* arm64 supported
* Raspberry Pi tested
* multi-stage build


# Usage

Official [documentation](https://github.com/google/cadvisor)    

Example:
```
sudo docker run \
  --volume=/:/rootfs:ro \
  --volume=/var/run:/var/run:ro \
  --volume=/sys:/sys:ro \
  --volume=/var/lib/docker/:/var/lib/docker:ro \
  --volume=/dev/disk/:/dev/disk:ro \
  --publish=8080:8080 \
  --detach=true \
  --name=cadvisor \
  --privileged \
  --device=/dev/kmsg \
  gcr.io/cadvisor/cadvisor:$VERSION


```

# Links
* github : https://github.com/dmitryboiadji/cadvisor-pi
* docker hub : https://hub.docker.com/r/dmitryboiadji/cadvisor-pi
* official registry : gcr.io/cadvisor/cadvisor