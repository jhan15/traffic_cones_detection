# traffic_cones_detection

It's a project to detect traffic cones and recognize the colors as well. I used [yolov5](https://github.com/ultralytics/yolov5) to train and detect cones.

## Dataset and annotation

I used a self-collected cone dataset. Thus, I also need to annotate the images myself. Here, I utilized an online annotation website [Roboflow](https://roboflow.com/), it provides services such as annotation, pre-processig, and augmentation. However, it has limitation of 1,000 source images and 5,000 generated images for free users.

## Model

```bash
Model
├── detection: yolov5s
└── color recognition: dominant color of buttom half of the detection box
```

## Usage

You can try the codes in colab if you are interested in. For prediction, I customized some files of yolov5, which are located in [utils](https://github.com/jhan15/traffic_cones_detection/tree/master/utils) folder, you need to use them when trying the codes.

- Train [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jhan15/traffic_cones_detection/blob/master/train.ipynb)

- Predict [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jhan15/traffic_cones_detection/blob/master/predict.ipynb)

## Result

<img src="https://user-images.githubusercontent.com/62132206/118353597-5d822000-b567-11eb-9e09-dd39bc877487.jpeg" height="300">
<img src="https://user-images.githubusercontent.com/62132206/118353605-62df6a80-b567-11eb-9bc0-4983853664b0.jpeg" height="300">
<img src="https://user-images.githubusercontent.com/62132206/118353609-683cb500-b567-11eb-8dd3-9624d8382d5f.jpeg" height="300">
<img src="https://user-images.githubusercontent.com/62132206/118353614-6a9f0f00-b567-11eb-81bd-bc4234948a0e.jpeg" height="300">
<img src="https://user-images.githubusercontent.com/62132206/118353625-75f23a80-b567-11eb-98c5-919eba29bdda.jpeg" height="300">
