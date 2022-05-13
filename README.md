# naive-cnn-detector
simple and slow cnn detector

This repo contains my examaples of using opencv and CNN (keras) for item detection. There is/will be examples of self-made-detector code. I dont wanna use pre-fitted solutions, my interest in building own decision from simple to progress.

## 1. Sliding window + cnn predict
Each of images is cut into many sqares, then each of them is checked by the model. If model says yes - print the rectangle.
This image shows the approved squares of image by model, squares containing shape of a car how to model said.
![approved ractengles](https://github.com/OneL1ght/naive-cnn-detector/blob/main/cifar1_screensh.png)

## 2. MOG substraction, detection in action
On the video of traffic all the cars is moving. So we dont need to slide around the frame. We just find moving objects and check them by model. If detected area is a car - show rectangle on this frame. The video is played in 24 fps, but in the realtime 8-sec video was playing for almost [3 minutes](https://github.com/OneL1ght/naive-cnn-detector/blob/main/realtime_detection.mp4)

![mog-detection-video](https://github.com/OneL1ght/naive-cnn-detector/blob/main/car_detection_cifar10__2.mp4)
