# Udacity_Self_Driving_Car_Project

# **Finding Lane Lines on the Road** 

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* To make use of the tools we learned in the lesson to identify lanes lines on the road
* Develop a pipeline that finds lane lines on the road on individual images
* Later apply the result to a video strem (really just series of images).


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describing my pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I defined canny to apply Canny Transform 
inorder to get edges of the image. After Canny I applied the gaussian_blur to smooth the edges using kernel_size 5.
And then I used the region_of_interest to get the interested area only and blacken the remaining area.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by listing out all x and y coordinates
and then using these coordinates I tried to find out whether the slope is positive or negative and updated it accordingly.
After that I averaged coordinates for both x and y, then calculated the slope denominator and deifined the y_min and y_max.
Finally I started checking whether the slope which I am trying to find out is whether valid or not and then used the most recent coordinates 
to draw the lines



### 2. Potential shortcomings current pipeline


One potential shortcoming would be what would happen when the video is taken in rainy or stormy whether
.


### 3. Possible improvements 

A possible improvement would be to that we should use our model on other color lane too, a here its focussed on white and yellow only
