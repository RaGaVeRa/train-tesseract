# train-tesseract
Dockerized example to train Tesseract v. 4

## Build Docker image:
```
$ docker build -t train-tesseract .
```
## Run Docker image:
```
$ docker run -it -v $PWD:/app --name train-tesseract train-tesseract /bin/bash
```
