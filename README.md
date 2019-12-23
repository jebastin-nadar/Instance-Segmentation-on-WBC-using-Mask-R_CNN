# Instance Segmentation using Mask R-CNN

There are various techniques that are used in computer vision tasks such as classification, semantic segmentation, object detection and instance segmentation. Instance Segmentation is identifying each object instance for every known object within an image. It assigns a label to each pixel of the image.

![person](https://user-images.githubusercontent.com/47391270/71358534-54c62e00-25af-11ea-8ff1-bf788c22b6c8.png)

### What is Mask R-CNN ?

The Mask R-CNN algorithm was introduced by He et al. in their 2017 paper, [*Mask R-CNN*](https://arxiv.org/abs/1703.06870). It is an instance segmentation technique which locates each pixel of every object in the image instead of the bounding boxes. It has three main stages:
1. **Backbone network** which is a standard CNN such as ResNet50 or ResNet101 is used to generate the feature maps.
2. **Region proposal network (RPN)** to propose candidate object bounding boxes.


