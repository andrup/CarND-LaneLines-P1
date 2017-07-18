# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Description of the imagae processing pipeline. 


My pipeline consists of 5 steps. 

Step | Image
---- | -----
Start | ![Original](start.png)
1. Convert image to grayscale with the build in function | ![Grayscale](gray.png)
1. Smoothing out noise by using Gaussian Blur algorithm | ![Gaussian](gaussian.png)
1. Canny Edge detection | ![Canny Edge](canny.png)
1. Masking the region of interest | ![Region of interrst](region.png)
1. Run Hough line algorithm to find lines in the image | ![Hough](hough.png)


Do line classification: Calculate the slope of the lines, choose the two highest slopes left and right. Only choose lines that have are within 80% of the slope of the highes and lowest slope.
Calculate mean slope and intercept and draw line between highest point and lower edge of the image.
Overlay with original picture. 

First, I converted the images to grayscale, then I .... 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...


![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
