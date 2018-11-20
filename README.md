# **Finding Lane Lines on the Road** 

## Writeup 

---



### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.


My pipeline was the following:

Input >>> Grayscale --> Gaussian Blur --> Canny edges --> Masking --> Hough Lines >>> Output

To improve the drawn_lines() function, I first separated the line segments into two lists (one for each line), then I used np.mean to find the average of all the segments.  I had to consider inverted y axis because of the way the image is represented.

Since, the vertical axis points(y1,y2) were already defined by the region of interest I only needed to find (x1,x2).

For this I used the slope-intercept form of the line equation, and with the averaged segment I extrapolated the full line. 



### 2. Identify potential shortcomings with your current pipeline

This pipeline is still very susceptible to variability in the images.


### 3. Suggest possible improvements to your pipeline

The parameters could be better tuned. 

Introduce other available image processing techniques to the pipeline.

Introduce an averaging method to get smoother lines.
