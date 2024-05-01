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
## NAME: LOKESH RAHUL V V 
## REG.NO:212222100024
### Convert image to grayscale and remove noise

```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("dog.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## Sobel edge detection:
### Sobel x axis:

```python
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
Sobel y axis:

```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
###Sobel xy axis:

```python
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```

### LAPLACIAN EDGE DETECTOR:

```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### CANNY EDGE DETECTOR:

```python
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## SOBEL EDGE DETECTOR
### Sobel x axis:
![image](https://github.com/lokeshrahulv/EDGE-DETECTION/assets/118423842/d5aa83ce-88f5-466a-be80-aae2a09a4098)

### Sobel y axis:
![image](https://github.com/lokeshrahulv/EDGE-DETECTION/assets/118423842/5b6621bc-4e2a-40f3-b995-9d6c948838b0)

### Sobel xy axis:
![image](https://github.com/lokeshrahulv/EDGE-DETECTION/assets/118423842/cda79191-0c2c-42e8-8f52-cc58e5f1545f)

### LAPLACIAN EDGE DETECTOR
![image](https://github.com/lokeshrahulv/EDGE-DETECTION/assets/118423842/84f64d39-576e-46eb-bb96-4cd6235a40e9)

### CANNY EDGE DETECTOR
![image](https://github.com/lokeshrahulv/EDGE-DETECTION/assets/118423842/ee3dbb62-f5a3-4a30-bde8-ebb1ad52b8cf)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
