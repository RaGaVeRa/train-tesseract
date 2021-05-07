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

## Clone tesstrain
```
# cd /app/src
# git clone https://github.com/tesseract-ocr/tesstrain.git
```

## Copy training data
```
# mkdir -p /app/src/tesstrain/data/kn2-ground-truth
# cp -a /app/data/ground-truth/* /app/src/tesstrain/data/kn2-ground-truth/.
```

## Train
```
# cd /app/src/tesstrain/
# make training MODEL_NAME=kn2 START_MODEL=kan PSM=7 TESSDATA=/usr/local/share/tessdata
```

## Copy trained model
```
# cp /app/src/tesstrain/data/kn2.traineddata /usr/local/share/tessdata/
```
