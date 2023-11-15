# dockerfiles-ubuntu-user-adderable
Ubuntu, It support base user creation and password setting.

# Building & Running

Copy the sources to your docker host and build the container, and to run.
```
	docker build   --rm -t sungjuko/ubuntu:v4 .
	docker run -it --rm --name u1  sungjuko/ubuntu:v4
```
Get the port that the container is listening on:

```
# docker ps
CONTAINER ID        IMAGE                COMMAND             CREATED             STATUS              PORTS               NAMES
fc199e02d300        sungjuko/ubuntu:v4   "/bin/bash"         41 seconds ago      Up 40 seconds                           u1
```

To test, ("sungjuko" is username. )
```
	tree
```
To Rollback
```
    docker rm u1 -f
    docker rmi sungjuko/ubuntu:v4
```
