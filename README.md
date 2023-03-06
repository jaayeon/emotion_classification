# Analysis of Understanding Using Deep Learning Facial Expression Recognition for Real Time Online Lectures
The purpose of this repository is to explore Degree Of Understanding(DoU) with deep learning in real time.

[paper](http://koreascience.or.kr/article/JAKO202006763002291.page)

[reference code](https://github.com/XiaoYee/emotion_classification)

## Environment
        python 3.7.4
        pytorch 1.2.0


## Detection Models
        1. Haar_cascade
        2. Blazeface
        3. DNN
        4. HOG
        5. MMOD
        6. MTCNN 


## Classification Models
        1. VGG
        2. VGG_GRU
        3. RESNET_GRU


## Dataset
reclassify FER2013, JAFFE, KDEF
```
        DATASET
        │  
        └───Not Understand(4,327)
        │   
        └───Neutral (2,176)
        │   
        └───Understand(3,378)
```

## Performance
all the performance train and test on FER2013, JAFFE, KDEF train and validation partition. 
speed [sec/4frame]


Model        |VGG             |  VGG+GRU | Resnet+GRU                 | 
--------     | --------       | -------- |  --------                  |
precision    | 49.8%          |   82.7%  |    94.3%                   |


test with private video
Model        |  Detection speed  |  Classification speed  |    sum    | 
--------     | --------       | -------- |  --------                  |
blazeface    | 0.089          |   0.281  |    0.370                   |
dnn(opencv)  | 0.209          |   0.278  |    0.487                   |
mmod(dlib)   | 13.181         |   0.316  |    13.50                   |
haar(opencv) | 0.244          |   0.265  |    0.509                   |
mtcnn        | 0.648          |   0.283  |    0.931                   |
hog(dlib)    | 0.149          |   0.301  |    0.450                   |
