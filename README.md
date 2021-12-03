# [CVDL] Training models to find 🥑 and 🐍
Hello! Here's a short story about how we trained YOLOv4, YOLOv5, and Mask-RCNN models, and benchmarked them on dataset of Avocados (🥑) and Cavas (🐍).
> *Avocado contains more fat than any other vegetable* 🥑

## Datasets

Let's kick off by describing two types of datasets we had for training: one for YOLO family of models and one for Mask RCNN as it requires not just bounding boxes (as YOLO do) but actual segmentaion masks. Pictures of our lovely plushies were taken all around the University of Innopolis (dormitories included) 🗺️.

### YOLO models

For training YOLOv4 and YOLOv5 it was enough just to annotate bounding boxes with 🥑 and 🐍 on [roboflow](https://roboflow.com/) and use the download link in the Colab notebook to retrieve the dataset. It's labelled version looks like this:

![image](https://user-images.githubusercontent.com/54360024/144668961-5c573838-d9bb-4398-9e43-6cc04eb4fea2.png)

### Mask RCNN model

For this model we needed some instance segmentation labelling interface, and we gladly used [label studio](https://labelstud.io/) as it is free and allows cooperative labelling which made the work twice as fast. Labelled avocados 🥑 look somewhat like this:

![image](https://user-images.githubusercontent.com/54360024/144669854-03cd9e04-5a7a-4376-b482-a9964b140f2c.png)

## Training 

Very sequential and straightforward. Little changes were made to original notebooks 👍.

## Results

> *Legends say that metrics values are provided in the notebooks* 🤓

No words needed. Let's just look at how trained models detected those cuties:


### YOLOv4

![image](https://user-images.githubusercontent.com/54360024/144670428-bbb6165c-861d-4d94-933c-1f5d57b97a2c.png)

### YOLOv5

![image](https://user-images.githubusercontent.com/54360024/144670456-a55c802e-9470-417f-afcb-de18b7e8800f.png)

### Mask RCNN

![image](https://user-images.githubusercontent.com/54360024/144670484-5587e659-9aac-4f4b-bd45-b3e80bb12de9.png)

## How to run

### YOLOv4 
No speacial things needed. Just download the notebook, and run all cells, shoud be ok 🤔.

### YOLOv5
Yep. Nothing special needed too. All the links and downloads are provided in the ipynb 🤙.

### Mask RCNN
Things get a bit tricky here as we didn't train it on dataset which was labeled on [roboflow](https://roboflow.com/), we used [label studio](https://labelstud.io/) instead, and to have the notebook working, you need to have [this dataset](https://drive.google.com/file/d/1RGh_CEb9JXmRkNYpXpeqtUtJ2fY4Bajg/view?usp=sharing) on your google drive. That's it 🙃.

## References

All models were training according to the official Colab tutorials on [roboflow](https://roboflow.com/) and [PyTorch](https://pytorch.org/):

* [YOLOv4](https://colab.research.google.com/drive/1b08y_nUYv5UtDY211NFfINY7Hy_pgZDt)
* [YOLOv5](https://colab.research.google.com/drive/1gDZ2xcTOgR39tGGs-EZ6i3RTs16wmzZQ)
* [Mask RCNN](https://pytorch.org/tutorials/intermediate/torchvision_tutorial.html)
