# SCW Module 1: A YOLO-based Automated System for Real-time 3D Printer State Monitoring
This is the object detection module for the Smart Connect Worker project funded and supervised by California State University Northridge Department of Energy.
This is the Python implementation regarding the YOLO-based object detection model as well as the machine state filtering algorithm as proposed in the published [ICCS 2021 conference paper](https://drive.google.com/file/d/1dvMl7bOjjt8JzsBF6P7kSXNZ-KeLhodt/view?usp=sharing) by Bian et. al. 
This work is largely based on the object detection model of [YOLOv3](https://github.com/eriklindernoren/PyTorch-YOLOv3).

## Summary (Detailed methodoly is in the paper)
![Screenshot](workflow.png)
The proposed work consists of two main parts: the first part is a YOLO-based object detection model that is able to detect and output the relative coordinates of the major components of a 3D printer; the second part is a filtering algorithm that takes as the input the coordinates predicted by the first module, and filters out the current machine state from all possible machine states by analyzing the coordinates. Finally, the raw and processed images as well as the predictions are displayed on a web-based graphical user interface (which is not included in this repository). All modules function in real-time, which allows spontaneous detections and monitoring of machine states.

## Part 1: YOLO-based object detection
We pre-trained a YOLOv3 model using images collected during an experiment in which the 3D printer of interest printed a sample model. During real-time testing, raw images acquired from a camera located inside the 3D printer are fed into the pretrained model, which produces the processed images with bounding boxes around each major component, as well as the coordinates of the detected components in pixels.

## Part 2: Filtering algorithm


## File Discriptions

Note: You may download the pre-trained weights [here](https://drive.google.com/file/d/1h2eFIRpB2K5esNt6qKxO1HiZ8V7e3kFm/view?usp=sharing), and put it into a folder named "weights".
