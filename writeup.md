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
[image_notexture]: ./test_images_output/whiteCarLaneSwitch.jpgnotexture.jpg
[image_gray]: ./test_images_output/whiteCarLaneSwitch.jpggray.jpg
[image_blur]: ./test_images_output/whiteCarLaneSwitch.jpgblur.jpg
[image_canny]: ./test_images_output/whiteCarLaneSwitch.jpgcanny.jpg
[image_mask]: ./test_images_output/whiteCarLaneSwitch.jpgmask.jpg
[image_hough]: ./test_images_output/whiteCarLaneSwitch.jpghough.jpg
[image_result]: ./test_images_output/whiteCarLaneSwitch.jpgresult.jpg

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I .... 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image_notexture]
![alt text][image_gray]
![alt text][image_blur]
![alt text][image_canny]
![alt text][image_mask]
![alt text][image_hough]
![alt text][image_result]


### 2. Identify potential shortcomings with your current pipeline

A potential shortcoming would be low contrast while the image becoming too bright or due to light-color lines.
Another would be different surface of roads. Ther are roads that has cross lines or bright textures that would cause problems.



### 3. Suggest possible improvements to your pipeline

There are some possible improvements.
1. Use another filter for better performance. Bilateral Filter is slow, so it would be a improvement if used better filters.
2. Stablize line fitting results. The result of line fitting looks not perfect. A possible improvement would be looking for better parameters and determine better samples.

