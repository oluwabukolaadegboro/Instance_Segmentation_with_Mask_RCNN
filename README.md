## Mask_RCNN

This also consitutes a part of my computer vision coursework taught by Georgia Gkioxari (a research scientist at Facebook) during my African Masters in Machine Intelligence (AMMI) program at AIMS Rwanda.

In this project, a nuts custom dataset was prepared and trained on an object detection library (Detectron2). The nuts dataset had 3 classes: date, fig and hazelnut, all annotated with instance masks. The dataset can be gotten here. The data contained an image directory which has the images, a train.json file that contains the train annotations in COCO format, and a val.json file that contains the val annotations in COCO format.

After preparing and registering the data, it was with trained a Mask R-CNN model with a ResNet50 feature Pyramid Network (FPN) backbone. I initialized the model with two initialization schemes: a scheme with an existing model pre-trained on the COCO dataset and a scheme with ImageNet weight. Finally, I trained for 300 iterations using a start learning rate of 0.002, 2 images per batch, and 128 regions per batch. Below are some of my visualizations I came across during the implementation of this work.


**Visualization of the both predictions for CocoNet initialization (right) and ImageNet initialization (left) on the validation set**

![CocoNet_and_ImageNet_predictions](/Images/CocoNet_and_ImageNet_predictions.png)   


**CocoNet Initialization AP Evaluation**

![COCO_initialization_AP_evaluation](/Images/COCO_initialization_AP_evaluation.png)  



**ImageNet Initialization AP Evaluation**
![ImageNet_initialization_AP_evaluation](/Images/ImageNet_initialization_AP_evaluation.png)  
