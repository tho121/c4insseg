# c4insseg
Train and export instance segmentation model using Detectron2 Go and export for mobile. Detects columns and colored pieces for Connect 4


This project aims to build an end-to-end pipeline for training an instance segmentation model to detect the state of a Connect 4 board and export it for PyTorch Mobile.
The instance segmentation model is trained using the Detectron2 Go framework (https://github.com/facebookresearch/d2go). Using the Faster-RCNN algorithm, the model is trained on a custom dataset of images taken from a Pixel 6 and resized to 510x384. Annotations are expected to be in the COCO format. This custom dataset was annotated manually using CVAT (https://www.cvat.ai/). After training, new images can be quickly annotated using label_from_predict.ipynb to generate more data. However, these annotations should not be perfect and should be uploaded to CVAT where they can be manually amended.


The c4_d2go.ipynb notebook trains and exports the model for PyTorch Mobile as the d2go_mobile_opt.ptl file. Copy this file to the Android assets folder. 
