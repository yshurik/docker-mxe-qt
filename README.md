# Create Docker image with MXE Qt ready

Docker image with MXE Qt ready can be prepared from ```yshurik/mxe``` docker image in next steps:

1. Use docker run to build the Qt in MXE container:

```docker run -it --privileged yshurik/mxe:debian-based-1 /bin/sh -c "make MXE_TARGETS=\"\$TARGETS\" qt5"```

2. When completed, find out finished container id with ```docker ps -a``` and do: 

```docker commit {container_id} mydockerhubuser/mxe-qt:build-1```

3. The image can be pushed to dockerhub, the container can be removed
