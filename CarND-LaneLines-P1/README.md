# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

Project 
---

The goals of this project were the following:
1. Make a pipeline that finds lane lines on the road.
2. Reflect on my work in a written report.


To identify lane markings on road images and videos, I adopted the following pipeline. For every road image, I:
1. Converted the image to gray scale to reduce it to one color channel.
2. Applied a Gaussian blur to the image.
3. Found the edges of the image by applying the Canny edge detection algorithm.
4. Defined the region of interest by applying a triangular polygon on the image.
5. Found the lane markings by applying the Hough Transform algorithm on the image.
6. Extrapolated the lane markings by fitting their coefficients to the equation of a straight line to deduce their resultant x-coordinate(s) in the form x=(y-c)/m.
7. Weighted the image on top of the original RGB image to give a clear representation of the position of lane markings.

 a) To find lane lines in a video stream, I apply all the above steps to individual frames of the video stream.


A potential shortcoming of my pipeline is that it is unable to accurately detect lane markings in cases where a vehicle has more than two lane lines in its region of interest.

To improve this pipeline, one would consider automating the process of calculating the image’s region of interest.
# 
  
  

###### Happy Hacking,
Gerry.


