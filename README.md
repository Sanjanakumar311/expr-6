# expr-6
# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:

DEVELOPED BY : SANJANA K L

REGISTER NUMBER : 212224230241
``` py
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Tiger.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
<img width="321" height="562" alt="image" src="https://github.com/user-attachments/assets/ed5cb084-5b22-4f8e-a8ba-a892fce50900" />


### SOBEL EDGE DETECTOR
``` py
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
<img width="317" height="550" alt="image" src="https://github.com/user-attachments/assets/0d0045b3-8b6e-4bd1-a5d3-53bacff14c2d" />


### LAPLACIAN EDGE DETECTOR
``` py
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
<img width="328" height="541" alt="image" src="https://github.com/user-attachments/assets/34356cca-728c-43c9-b1ad-83620838d180" />


### CANNY EDGE DETECTOR
``` py
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
<img width="312" height="528" alt="image" src="https://github.com/user-attachments/assets/17033558-13cb-4301-a0f8-e8ca846a30c4" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
