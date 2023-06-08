## EX.NO: 07 <br>
## DATE: 
# <p align="center">EDGE DETECTION</p>

## Aim:

To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:

Anaconda - Python 3.7

## Algorithm:

### Step1:
Import the necessary modules.
<br>


### Step2:
For performing edge detection on a image.

* Sobel

* Laplacian

* Canny

<br>

### Step3:
Display all the images with their respective edge detected images.
<br>
 
## Program:

``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread ('eye.jpg') 
gray_image = cv2.cvtColor(image1,cv2.COLOR_BGR2GRAY)

plt.title('GRAY IMAGE')
plt.imshow(gray_image,cmap = 'gray')

img = cv2.GaussianBlur(gray,(3,3),0)
sobelx = cv2.Sobel(gray_image,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(gray_image,cv2.CV_64F,0,1,ksize=5)
sobelxy =cv2.Sobel(gray_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(1)
plt.subplot(2,2,1)
plt.imshow(gray_image,cmap = 'gray')
plt.title('Original'), plt.xticks([]), plt.yticks([])

plt.subplot(2,2,2)
plt.imshow(sobelx,cmap='gray')
plt.title('sobelx')
plt.xticks([]), plt.yticks([])

plt.subplot(2,2,3)
plt.imshow(sobely,cmap='gray')
plt.title('sobely')
plt.xticks([]), plt.yticks([])

plt.subplot(2,2,4)
plt.imshow(sobelxy,cmap='gray')
plt.title('sobelxy')
plt.xticks([]), plt.yticks([])
plt.show()
# cv2.waitKey(0)
laplacian = cv2.Laplacian(gray_image,cv2.CV_64F)
plt.imshow(laplacian,cmap='gray')
plt.title('laplacian')
plt.show()

canny_edges = cv2.Canny(gray_image, 120, 150)
plt.imshow(canny_edges,cmap='gray')
plt.title('canny_edges')
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR

![image](https://user-images.githubusercontent.com/74660507/168250944-6e2aa80d-4239-49e0-85bc-bd3122deb6f6.png)


### LAPLACIAN EDGE DETECTOR

![image](https://user-images.githubusercontent.com/74660507/168251049-cc8d14c5-0eb7-4b4c-8646-8fd50218e1d3.png)


### CANNY EDGE DETECTOR

![image](https://user-images.githubusercontent.com/74660507/168251139-26253bd3-88e0-4dc3-9471-1180535e9431.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
