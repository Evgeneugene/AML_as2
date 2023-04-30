# Faster RCNN/Yolovx assignment

Evgenii Evlampev, B20-AI, e.evlampev@innopolis.university

## 1. Data

I used the same data from previous assignmen - 200 photos of both dogs and cats from this dataset:
[https://www.kaggle.com/datasets/shaunthesheep/microsoft-catsvsdogs-dataset](https://www.kaggle.com/datasets/shaunthesheep/microsoft-catsvsdogs-dataset)

## 2. Annotating 

Then I annotated segmentations for the data by hand on [roboflow.com](roboflow.com), preprocessed and augmented it by some modifications from 200 to 480 instances. You can check it by this link:
[https://universe.roboflow.com/w-68qqu/cats-dogs-segmentation/dataset/1](https://universe.roboflow.com/w-68qqu/cats-dogs-segmentation/dataset/1)

## 3. Training Mask RCNN model using detectron2

The code was taken from this link with little changes (dataset and some training parameters):
[https://roboflow.com/model/mask-rcnn](https://roboflow.com/model/mask-rcnn)

## 4. Training Yolov8

The same applies to Yolov8, the code was taken from [https://colab.research.google.com/github/roboflow-ai/notebooks/blob/main/notebooks/train-yolov8-object-detection-on-custom-dataset.ipynb?ref=roboflow-blog](https://colab.research.google.com/github/roboflow-ai/notebooks/blob/main/notebooks/train-yolov8-object-detection-on-custom-dataset.ipynb?ref=roboflow-blog) with changed dataset and model (Yolov8n-seg - the smallest).

## 5. Evaluating models

- mAP50 for YOLOv8n is equal to 0.495, whereas for Mask RCNN using detectron2 is euqal to 0.74.

- Overall training speed for Mask RCNN: 1899 iterations in 0:11:50 (2.67 s / it).
- Speed for YOLOv8n-seg: 1.10it/s

