# naive-cnn-detector
simple and slow cnn detector

This repo contains my examples of using `opencv` and CNN (`keras`) for item detection. There is/will be examples of self-made-detector code. I dont wanna use pre-fitted solutions, my interest is in building own decision from simple to progress.

## 1. Sliding window + cnn predict
Each image is cut into many sqares, then each of them is checked by the model. If model says "yes" - rectangle is printed.
This image shows the approved squares by model, containing shape of a car as model said.

![approved ractengles](https://github.com/OneL1ght/naive-cnn-detector/blob/main/cifar1_screensh.png)

## 2. MOG substraction, detection in action
On the video of traffic all the cars are moving. So we dont need to slide around the frame. We just find moving objects and check them by model. If detected area is a car - rectangle on this frame is shown. The video is played in 24 fps, but in the realtime 8-sec video was playing for almost [3 minutes](https://github.com/OneL1ght/naive-cnn-detector/blob/main/realtime_detection.mp4). But anyway it is faster then 1st solution, where recognition on 5 photos took more then 3 minutes and result was not good.

![video-screenshot](https://github.com/OneL1ght/naive-cnn-detector/blob/main/with_mask.png)

The full ![video](https://github.com/OneL1ght/naive-cnn-detector/blob/main/car_detection_cifar10__2.mp4)
