# cmplopes/alpine-clang
clang 10.0.0-r2 over Alpine Linux 3.12

```
$ docker pull cmplopes/alpine-clang
```

## Suported Tags

[latest - (clang 10.0.0-r2 over alpine:3.12) (Dockerfile)](https://github.com/cmplopes/alpine-clang/blob/master/latest/Dockerfile)

## Check clang version
```
$ docker run --rm -it -v $(pwd):/source cmplopes/alpine-clang
```
or
```
$ docker run --rm -it -v $(pwd):/source cmplopes/alpine-clang clang --version
```

## Compile, link and run a c program
```
$ docker run --rm -it -v $(pwd):/source cmplopes/alpine-clang clang -Wall -o test /source/test.c
$ docker run --rm -it -v $(pwd):/source cmplopes/alpine-clang ./test
```
