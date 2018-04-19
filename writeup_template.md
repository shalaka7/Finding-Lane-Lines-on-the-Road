# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.


**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road.
* To track the lines.
* Reflect on your work in a written report


---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps.
1.convert into gray scale image.
2.Apply a Gaussian Noise kernel with kernel size 3.
3.Apply a canny filter for edge detection with suitable threshold value.
4.To find vertices, edges (i.e.which are obtain by canny filter )for region of interest.
5.Apply Hough transform function on edge detected image.


In order to draw a single line on the left and right lanes, I modified the draw_lines() function ,for modifing the function we have to know slope ,intercept, center of lines. We store all the values then we average all the value we get the single number for all the parameter.We divide all parameter by right and left section and finally we draw line by using liner regrresion funtion

Sample output image

![alt text][http://localhost:8888/view/Self%20Driving%20Car%20Codebase/udacity_project_1/test_images/output_solidWhiteCurve.jpg]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be line which are drawn they are blinking but when will change thickness of line it is constant.




### 3. Suggest possible improvements to your pipeline

A possible improvement would be to modify the algorithm for video having curve paths.

