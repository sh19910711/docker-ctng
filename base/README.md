```
$ docker build -t ctng .
$ docker run --rm --name ctng -ti ctng bash
$ docker exec -ti ctng ct-ng menuconfig
$ docker exec cat .config > path/to/.config
```
