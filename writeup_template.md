# **Finding Lane Lines on the Road** 

## Writeup Template

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

The goal of this project is to detect lanes in a given picture first and then on a video. Two main cv functions here are Canny Edge detection and Hough Transform. 

My pipeline consisted of 5 steps. First, read in the image and then  converte to grayscale.Nest step is to apply Canny edge method to take the gradient of the image and leaving only boundaries of the objects. Then cropping the unwanted parts and keeping region of interest. Last step is to apply Hough transform. Need to play with hough parameters to find the best possible lane layout. Last to apply to the video frame.


### 2. Identify potential shortcomings with your current pipeline

My pipeline worked pretty well with first visedo but not much for the second video as it was more curvy.
Practical view:I still think only relying on lanes won't be enough for lane detection as the lanes could be unclear due to road conditions or light.


### 3. Suggest possible improvements to your pipeline

I think for curves we might need some sort of calibration as they hard to fit in a line.

Practical: Would be good to have a sense of distance and not just relying on lanes in order for the car to stay in lanes. Hence, if lane is unclear in parts of the road car still can stay on the lane by keeping the proper distance.
