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
## Developed by: Tirupathi Jayadeep
## Register Number: 212223240169

```p
import cv2
import matplotlib.pyplot as plt

image=cv2.imread('flower.jpg',0)
```
```p
gray_image=cv2.cvtColor(image,cv2.COLOR_GRAY2RGB)
gray_image=cv2.GaussianBlur(gray_image,(3,3),0)
```
## Sobel X Axis
```p
sobelx=cv2.Sobel(gray_image,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
## Sobel Y Axis
```p
sobely=cv2.Sobel(gray_image,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
## Sobel XY Axis
```p
sobelxy=cv2.Sobel(gray_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LaplacianEdge Detector
```p
lap=cv2.Laplacian(gray_image,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## Canny Edge Detector
```p
canny=cv2.Canny(gray_image,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
## Sobel X Axis
![image](https://github.com/23004426/EDGE-DETECTION/assets/144979327/64589c6d-6eb8-4a27-a907-35bd34e9bed6)

## Sobel Y Axis
![image](https://github.com/23004426/EDGE-DETECTION/assets/144979327/98b8b499-73c4-416e-9eae-eaa570c2bba3)

## Sobel XY Axis
![image](https://github.com/23004426/EDGE-DETECTION/assets/144979327/d104cd92-1b7d-4a48-b716-1cc28806aab2)


### LAPLACIAN EDGE DETECTOR
![image](https://github.com/23004426/EDGE-DETECTION/assets/144979327/f74509a0-79d0-4734-8acb-51612fd39078)



### CANNY EDGE DETECTOR
![image](https://github.com/23004426/EDGE-DETECTION/assets/144979327/8aaaf1d5-cebf-4201-b0d2-ace9f724409c)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
