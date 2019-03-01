# FaceDetection_OpenCV_DNN
Face Detection using OpenCV DNN module

---

## Background

You may already know that OpenCV ships out-of-the-box with pre-trained Haar cascades that can be used for face detection…but you may not be knowing about the “hidden” deep learning-based face detector that has been part of OpenCV since OpenCV 3.3.

Back in August 2017, OpenCV 3.3 was officially released, bringing it with a highly improved “deep neural networks” ( dnn ) module. This module supports a number of deep learning frameworks, including Caffe, TensorFlow, and Torch/PyTorch.

## Contents

* How it works
* Finding “hidden” deep learning face detector in the OpenCV library
* Steps involved in face detection
* Performing face detection in images using OpenCV and deep learning
* Performing face detection in video using OpenCV and deep learning

## How it works

OpenCV’s deep learning face detector is based on the Single Shot Detector (SSD) framework with a ResNet base network (unlike other OpenCV SSDs that you may have seen which typically use MobileNet as the base network).

## Finding “hidden” deep learning face detector in the OpenCV library

When using OpenCV’s deep neural network module with Caffe models, you’ll need two sets of files:

The .prototxt file(s) which define the model architecture (i.e., the layers themselves)
The .caffemodel file which contains the weights for the actual layers
.prototxt files can be found in the GitHub repo. The weight files are not included in the OpenCV samples directory and it requires a bit more digging to find them…

## Steps involved in face detection

* Load the model
* Read the image and create a blob image
* Pass the blob through the network and get detections
* Loop over the detections, filter detections with less confidence and draw boxes around the detected faces

## Performing face detection in images using OpenCV and deep learning

In this first example we’ll learn how to apply face detection with OpenCV to single input images.

In the next section we’ll learn how to modify this code and apply face detection with OpenCV to videos, video streams, and webcams.

## Observations

It is impressed that OpenCV can detect faces despite the lighting conditions and shadows cast on the face in the dark venue (and with 86.81% probability!)

Again, this just goes to show how much better (in terms of accuracy) the deep learning OpenCV face detectors are over their standard Haar cascade counterparts shipped with the library.

## Reference

https://www.pyimagesearch.com/2018/02/26/face-detection-with-opencv-and-deep-learning/
