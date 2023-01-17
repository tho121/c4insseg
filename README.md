# Connect4 Action AI (Training Model)
Train and export instance segmentation model using Detectron2 Go and export for mobile. Detects columns and colored pieces for Connect4. App implementation found at https://github.com/tho121/c4android


This project aims to build an end-to-end pipeline for training an instance segmentation model to detect the state of a Connect4 board and export it for PyTorch Mobile.
The instance segmentation model is trained using the Detectron2 Go framework (https://github.com/facebookresearch/d2go). Using the Faster-RCNN algorithm, the model is trained on a custom dataset of images taken from a Pixel 6 and resized to 510x384. Annotations are expected to be in the COCO format. This custom dataset was annotated manually using CVAT (https://www.cvat.ai/). After training, new images can be quickly annotated using label_from_predict.ipynb to generate more data. However, these annotations should not be perfect and should be uploaded to CVAT where they can be manually amended.


The c4_d2go.ipynb notebook trains and exports the model for PyTorch Mobile as the d2go_mobile_opt.ptl file. Copy this file to the Android assets folder. 

# Training Metrics

Loss
![image](https://user-images.githubusercontent.com/4165980/208512453-f35d4375-39ee-4a33-96ae-85eadf2965c4.png)

Learning Rate
![image](https://user-images.githubusercontent.com/4165980/208513238-80d999ad-2c14-4daa-9150-8613f6e0ee2a.png)

Validation Metrics
![image](https://user-images.githubusercontent.com/4165980/208513389-ac0690df-27a2-4ae3-b74a-ed6de4625a43.png)
