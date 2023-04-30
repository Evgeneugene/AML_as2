# Faster RCNN/Yolovx assignment

Evgenii Evlampev, B20-AI, e.evlampev@innopolis.university

## 1. Data

I decided that it would simplier to download existing photos, so in my case it is the cats' and dogs' photos that the model should detect. 

I took 200 photos of both dogs and cats from this dataset:
[https://www.kaggle.com/datasets/shaunthesheep/microsoft-catsvsdogs-dataset](https://www.kaggle.com/datasets/shaunthesheep/microsoft-catsvsdogs-dataset)

## 2. Annotating 

Then I annotated the data by hand on [roboflow.com](roboflow.com), preprocessed and augmented it by some modifications from 200 to 480 instances. You can check it by this link:
[https://app.roboflow.com/w-68qqu/cats-dogs-6zm8r/2](https://app.roboflow.com/w-68qqu/cats-dogs-6zm8r/2)

## 3. Training Faster RCNN model using detectron2

The code was taken from this link with little changes (dataset and some training parameters):
[https://blog.roboflow.com/how-to-train-detectron2/](https://blog.roboflow.com/how-to-train-detectron2/)

## 4. Training Yolov8

The same applies to Yolov8, the code was taken from [https://colab.research.google.com/github/roboflow-ai/notebooks/blob/main/notebooks/train-yolov8-object-detection-on-custom-dataset.ipynb?ref=roboflow-blog](https://colab.research.google.com/github/roboflow-ai/notebooks/blob/main/notebooks/train-yolov8-object-detection-on-custom-dataset.ipynb?ref=roboflow-blog) with changed dataset and model (Yolov8n - the smallest).

## 5. Evaluating models

- mAP50 for YOLOv8n is equal to 0.694, whereas AP for Faster RCNN using detectron2 is euqal to 54.857.

- Overall training speed for Faster RCNN: 597 iterations in 0:20:15 (2.0356 s / it).
- Speed for YOLOv8n: 0.3ms pre-process, 7.7ms inference, 0.0ms loss, 1.8ms post-process per image.

