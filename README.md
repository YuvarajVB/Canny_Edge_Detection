# Canny_Edge_Detection_using_OpenCV

## AIM
To implement the Canny Edge Detection algorithm on a sample image using Python and observe how different parameters affect the edge detection results.

## PROCEDURE
1. Import Required Libraries Import OpenCV, NumPy, and Matplotlib for image processing and visualization.
2. Load the Input Image Read the sample image using cv2.imread().
3. Convert to Grayscale Convert the image to grayscale for intensity-based processing.
4. Apply Gaussian Blur Apply Gaussian smoothing (e.g., kernel size 5×5) to reduce noise and avoid false edge detection.
5. Apply Canny Edge Detector Use the cv2.Canny() function with chosen lower and upper threshold values.
6. View and Compare Results Plot the original, blurred, and edge-detected images using Matplotlib.
7. Experiment with Parameter Variations Change Gaussian kernel sizes and threshold values to observe differences in detected edges.

## Program
```py
import cv2
import matplotlib.pyplot as plt
import numpy as np
img = cv2.imread("elephant.jpg")
plt.imshow(img)
blur_img = cv2.blur(img,ksize=(25,25))
plt.imshow(blur_img,cmap='gray')
medium = np.median(img)
low = int(max(0,0.7*medium))
high = int(max(255,(1/3)*medium))
cany_edge = cv2.Canny(img,threshold1=low,threshold2=high)
plt.imshow(cany_edge,cmap='gray')
```
## RESULT
The Canny edge detection algorithm successfully extracted clear and sharp edges from the input image.
