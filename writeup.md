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

My pipeline consisted of 7 steps.

1. Bilateral Filterring
Since I am looking for lane lines, it's best that remaining the contrast of edges while blurring.
After diving in OpenCV, I found a filter that meet this requirement. I call this step "removing texture"

![alt text][image_notexture]

2. Conver blurred image to gray scale.

![alt text][image_gray]

3. Gaussian Blur

![alt text][image_blur]

4. Find Canny edge

![alt text][image_canny]

5. Apply mask

![alt text][image_mask]

6. Find hough lines
In this step, I modified the draw_lines() function by fitting a line with line tips in order to draw a single solid line per lane.

![alt text][image_hough]

a. red lines are hough lines
b. green lines are best fitting lines.

7. Finally, draw solid lines on original image.

![alt text][image_result]



### 2. Identify potential shortcomings with your current pipeline

A potential shortcoming would be low contrast while the image becoming too bright or due to light-color lines.
Another would be different surface of roads. Ther are roads that has cross lines or bright textures that would cause problems.



### 3. Suggest possible improvements to your pipeline

There are some possible improvements.
1. Use another filter for better performance. Bilateral Filter is slow, so it would be a improvement if used better filters.
2. Stablize line fitting results. The result of line fitting looks not perfect. A possible improvement would be looking for better parameters and determine better samples.

