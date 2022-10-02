<h1 align="center">Driver Drowsiness Detection

## Description 📌

A computer vision system that can automatically detect driver drowsiness in a real-time video stream and then alert if the driver appears to be drowsy.

## Applications 🎯
This can be used by drivers who tend to drive for a longer period of time that may lead to accidents.

## Dependencies

1) import cv2
2) import imutils
3) import dlib
4) import numpy

## Procedure
If a face is found, we apply facial landmark detection and extract the eye regions. 
Now that we have the eye regions, we can compute the eye aspect ratio to determine if the eyes are closed.
If the eye aspect ratio indicates that the eyes have been closed for a sufficiently long enough amount of time, it indicates that driver is drowsy.

Each eye is represented by 6 (x, y)-coordinates, starting at the left-corner of the eye, and then working clockwise around the eye.
It checks 20 consecutive frames and if the Eye Aspect ratio is less than 0.25, Alert is generated.
