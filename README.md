# Instance Segmentation using Mask R-CNN

There are various techniques that are used in computer vision tasks such as classification, semantic segmentation, object detection and instance segmentation. Instance Segmentation is identifying each object instance for every known object within an image. It assigns a label to each pixel of the image.

![person](https://user-images.githubusercontent.com/47391270/71358534-54c62e00-25af-11ea-8ff1-bf788c22b6c8.png)

### What is Mask R-CNN ?

The Mask R-CNN algorithm was introduced by He et al. in their 2017 paper, [*Mask R-CNN*](https://arxiv.org/abs/1703.06870). It is an instance segmentation technique which locates each pixel of every object in the image instead of the bounding boxes. It has three main stages:
1. **Backbone network** which is a standard CNN such as ResNet50 or ResNet101. It is used to generate the feature maps.
2. **Region proposal network (RPN)** to propose candidate object bounding boxes.It uses a CNN to generate the multiple Region of Interest(RoI) using a lightweight binary classifier. 
3. **RoI Align network** outputs multiple bounding boxes and warps them into a fixed dimension. Warped features are then fed into *fully connected layers* to make classification (using Softmax) and boundary box prediction (using regression). 
The features are also fed into *Mask classifier*, which consists of two CNN’s, to output a binary mask for each RoI. Mask Classifier generates masks for every class without competition among classes.
![mrcnn](https://user-images.githubusercontent.com/47391270/71436870-2febcb00-2715-11ea-937e-6bf3bf525517.png)
### Data

The images have been taken from the Leukocyte Images for Segmentation and Classification Database [(LISC)](http://users.cecs.anu.edu.au/~hrezatofighi/Data/Leukocyte%20Data.htm). 
![Screenshot from 2019-12-25 13-04-24](https://user-images.githubusercontent.com/47391270/71437336-38450580-2717-11ea-9732-4e39cc5c0147.png)
The images have to segmented into these 5 types of WBC's:
1. Basophil 
2. Eosinophil, 
3. Neutrophil
4. Lymphocyte
5. Monocyte


