Hand detection is a fundamental sub-task of object detection that has historically been hard to implement. But there have been many technological advancements in the field of machine learning and AI in recent years.
One of the core technologies widely used is TensorFlow, an end-to-end open-source platform for machine learning. It has a wide-ranging, flexible ecosystem of tools, libraries, and community resources. With the power of TensorFlow technology, researchers and developers can easily develop and deploy ML-powered applications.
Handtrack.js is a library for prototyping real-time hand detection (using bounding boxes), directly in the browser. This library is very useful for our cause in the implementation of this project. Behind the scenes, this library uses a trained convolutional neural network (CNN) that provides bounding box predictions for the location of hands in an image. The convolutional neural network (ssdlite, mobilenetv2) is trained using the TensorFlow object detection API.
![image](https://user-images.githubusercontent.com/85755206/127895263-79c71568-761b-4d16-80f6-e9ab1138e5a4.png)
![image](https://user-images.githubusercontent.com/85755206/127895289-f4c5812d-5cfb-4d99-984d-369f258f4aea.png)
![image](https://user-images.githubusercontent.com/85755206/127895496-ae4c4724-6fb1-46cb-8dd7-518423dcc451.png)
This is a tutorial on how to train a 'hand detector' with TensorFlow object detection API. This README outlines how to set up everything and train the object detection model locally. You could refer to the following blog post for more detailed description about the steps within.

https://jkjung-avt.github.io/hand-detection-tutorial/
https://github.com/victordibia/handtracking/blob/master/images/hand1.gif
https://github.com/victordibia/handtracking/blob/master/images/hand2.gif
https://github.com/victordibia/handtracking/blob/master/images/hand3.gif

Setup
Just for reference, the code in this repository has been tested on a desktop PC with:

NVIDIA GeForce GTX-1080Ti
Ubuntu 16.04.5 LTS (x86_64)
CUDA 9.2
cuDNN 7.1.4
TensorFlow 1.10.0
This tutorial uses python3 for training and testing the TensorFlow object detection models. Follow the steps below to set up the environment for training the models. Make sure tensorflow-gpu or tensorflow (python3 packages) has been installed on the system already.

Clone this repository.

$ cd ~/project
$ git clone https://github.com/jkjung-avt/hand-detection-tutorial.git
$ cd hand-detection-tutorial
Install required python3 packages.

$ sudo pip3 install -r requirements.txt
In case you are having trouble with sudo, you can do pip3 install --user -r requirements.txt instead.

Run the installation script. Make sure the last step in the script, Running model_builder_test.py, finishes without error, before continuing on.

$ ./install.sh
Download pretrained models from TensorFlow Object Detection Model Zoo.

$ ./download_pretrained_models.sh
You can then check out the output image by, say,

$ display detection_output.jpg
![image](https://user-images.githubusercontent.com/85755206/127896264-c562fdb7-7931-4d54-ab80-9adb24dfa1d6.png)
