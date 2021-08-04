[![GitHub issues](https://img.shields.io/github/issues/jhan15/traffic_cones_detection)](https://github.com/jhan15/traffic_cones_detection/issues)
![GitHub last commit](https://img.shields.io/github/last-commit/jhan15/traffic_cones_detection?color=ff69b4)

# traffic_cones_detection

It's a project to detect traffic cones and recognize the colors as well. I used [yolov5](https://github.com/ultralytics/yolov5) to train and detect cones. Furthermore, I used k-means to determine the dominant color to classify cone color. Currently, the supported colors are red, yellow, green, and blue. Other colors are classified as unknown.

## Dataset and annotation

I used a self-collected cone dataset with 303 cone images. It's not a perfect practice because it's a small dataset. I also need to annotate the images myself. Here, I utilized an online annotation website [Roboflow](https://roboflow.com/), it provides services such as annotation, pre-processig, and augmentation. However, it has limitation of 1,000 source images and 5,000 generated images for free users.

## Model

```bash
Model
├── cone detection: yolov5s
└── color recognition: dominant color (k-means)
```

## Usage

You can try the codes in colab if you are interested in. 

#### Train

If you have an annotated dataset, you can train directly use train.ipynb [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jhan15/traffic_cones_detection/blob/master/train.ipynb)

#### Prediction

If you want to detect cones directly, use predict.ipynb [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jhan15/traffic_cones_detection/blob/master/predict.ipynb)

You should use the weights I trained in [model](https://github.com/jhan15/traffic_cones_detection/tree/master/model). Besides, I customized some files of yolov5, which are located in [utils](https://github.com/jhan15/traffic_cones_detection/tree/master/utils) folder, you need to use them as well.

## Result

#### Video

I clipped a video from one research project of [ETH Zurich](https://www.trace.ethz.ch/publications/2019/TrafficCone/) to test the peroformance.

![cone1](https://user-images.githubusercontent.com/62132206/120334300-d1a31e80-c2f0-11eb-962e-17c4d5481917.gif)

#### Images

<img src="https://user-images.githubusercontent.com/62132206/118353597-5d822000-b567-11eb-9e09-dd39bc877487.jpeg" width="600">
<img src="https://user-images.githubusercontent.com/62132206/118353605-62df6a80-b567-11eb-9bc0-4983853664b0.jpeg" width="600">
<img src="https://user-images.githubusercontent.com/62132206/118353609-683cb500-b567-11eb-8dd3-9624d8382d5f.jpeg" width="600">
<img src="https://user-images.githubusercontent.com/62132206/118353614-6a9f0f00-b567-11eb-81bd-bc4234948a0e.jpeg" width="600">
<img src="https://user-images.githubusercontent.com/62132206/118353625-75f23a80-b567-11eb-98c5-919eba29bdda.jpeg" width="600">
<img src="https://github.com/jhan15/traffic_cones_detection/blob/master/images/3.jpeg" width="600">
<img src="https://github.com/jhan15/traffic_cones_detection/blob/master/images/6.jpeg" width="600">
