# EX- 6 EDGE-DETECTION
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
### PROGRAM
```
Developed by:SANDHIYA R
Register number:212222230129
```
```python
# import libraries
import numpy as np
import cv2
import matplotlib.pyplot as plt
# load the images
input_image=cv2.imread("rose.jpg")
image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.imshow(image)
#Color conversion
grey_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2GRAY)
img1=cv2.GaussianBlur(grey_image,(3,3),0)
# Sobel edge detection
sobelx = cv2.Sobel(img1,cv2.CV_64F,1,0,ksize=5) 
plt.figure(1)
plt.subplot(1,2,1)
plt.imshow(img1,cmap = 'gray')
plt.title('Original')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap = 'gray')
plt.title('sobel x')
plt.xticks([])
plt.yticks([])
plt.show()

sobely = cv2.Sobel(img1,cv2.CV_64F,0,1,ksize=5) 
plt.figure(1)
plt.subplot(1,2,1)
plt.imshow(img1,cmap = 'gray')
plt.title('Original')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap = 'gray')
plt.title('sobel y')
plt.xticks([])
plt.yticks([])
plt.show()
sobelxy = cv2.Sobel(img1,cv2.CV_64F,1,1,ksize=5) 
plt.figure(1)
plt.subplot(1,2,1)
plt.imshow(img1,cmap = 'gray')
plt.title('Original')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap = 'gray')
plt.title('sobel xy')
plt.xticks([])
plt.yticks([])
plt.show()
# Laplacian edge detection
laplacian = cv2.Laplacian(img1,cv2.CV_64F)
plt.figure(1)
plt.subplot(1,2,1)
plt.imshow(img1,cmap = 'gray')
plt.title('original')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap = 'gray')
plt.title('laplacian')
plt.xticks([])
plt.yticks([])
plt.show()
# Canny edge detection
canny_edges = cv2.Canny(img1, 120, 150)
plt.figure(1)
plt.subplot(1,2,1)
plt.imshow(img1,cmap = 'gray')
plt.title('original')
plt.subplot(1,2,2)
plt.imshow(canny_edges,cmap = 'gray')
plt.title('canny')
plt.xticks([])
plt.yticks([])
plt.show()

```

## Output:
### ORIGINAL IMAGE
![image](https://github.com/SandhiyaR1/EDGE-DETECTION/assets/113497571/e470cab2-de01-4fdd-aebb-d5953e10baeb)

### SOBEL EDGE DETECTOR

![output](./sobel.png)

### LAPLACIAN EDGE DETECTOR
![output](./laplacian.png)


### CANNY EDGE DETECTOR
![output](./canny.png)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
