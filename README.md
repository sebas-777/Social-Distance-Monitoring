# Social-Distance-Monitoring

## Introduction
This repository holds the implementation of monitoring social distancing implied for COVID-19 using  [YOLACT: Real-time Instance Segmentation](https://arxiv.org/abs/1904.02689)) for object detection. 

## User Guideline
**System Requirement**
- For better performance you will cuda version 10 or 10.1
 - Python3

**Installation**
```
	$ pip install -r requirements.txt
 ```
 #### For the installation of torch using "pip" kindly follow the instructions from [Pytorch](https://pytorch.org/)

First, you need to clone the repository using gitbash (if gitbash is already installed) or you can download the zip file.
```
	$ git clone https://github.com/paul-pias/Social-Distance-Monitoring.git
```

If want to see your output in your browser execute the "server.py" script or else run "inference.py" to execute it locally.

If you want to run the inference on a ip camera need to use **WebcamVideoStream** with the following command. 
```
	"rtsp://assigned_name_of_the_camera:assigned_password@camer_ip/"
```
If you want to use YOLACT++, compile deformable convolutional layers (from [DCNv2](https://github.com/CharlesShang/DCNv2/tree/pytorch_1.0)). Make sure you have the latest CUDA toolkit installed from [NVidia's Website](https://developer.nvidia.com/cuda-toolkit).
```
	cd external/DCNv2
	python setup.py build develop
```

In the official Yolact repository there are several pre-trained model available.
|    Image Size            |Model File                         |Config                         |
|----------------|-------------------------------|-----------------------------|
|550|[yolact_resnet50_54_800000.pth](https://drive.google.com/file/d/1yp7ZbbDwvMiFJEq4ptVKTYTI2VeRDXl0/view?usp=sharing)            |yolact_resnet50            |
|550          |[yolact_darknet53_54_800000.pth](https://drive.google.com/file/d/1dukLrTzZQEuhzitGkHaGjphlmRJOjVnP/view?usp=sharing)           |yolact_darknet53            |
|550          |[yolact_base_54_800000.pth](https://drive.google.com/file/d/1UYy3dMapbH1BnmtZU4WH1zbYgOzzHHf_/view?usp=sharing)|yolact_base|
|700|[yolact_im700_54_800000.pth](https://drive.google.com/file/d/1lE4Lz5p25teiXV-6HdTiOJSnS7u7GBzg/view?usp=sharing)            |yolact_im700            |
|550         |[yolact_plus_resnet50_54_800000.pth](https://drive.google.com/file/d/1ZPu1YR2UzGHQD0o1rEqy-j5bmEm3lbyP/view?usp=sharing)            |yolact_plus_resnet50            |
|550          |[yolact_plus_base_54_800000.pth](https://drive.google.com/file/d/15id0Qq5eqRbkD-N3ZjDZXdCvRyIaHpFB/view?usp=sharing)|yolact_plus_base|
