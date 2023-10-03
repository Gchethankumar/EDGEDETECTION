# EDGE DETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary modules.

### Step2:
For performing edge detection on a image.

#### .Sobel
sobelx=cv2.Sobel(gray,cv2.CV_64F,1,0,5)
sobely=cv2.Sobel(gray,cv2.CV_64F,0,1,5)
sobelxy=cv2.Sobel(gray,cv2.CV_64F,1,1,5)

#### .Laplacian
lap=cv2.Laplacian(gray,cv2.CV_64F)

#### .Canny
canny=cv2.Canny(gray,120,150)

### Step3:
Display all the images with their respective edge detected images.
 
## Program:
```
Developed by: G.Chethan Kumar
Register no : 212222240022
```

### Import the packages
``` Python
import cv2
import matplotlib.pyplot as plt
```

### Load the image, Convert to grayscale and remove noise
```python
img=cv2.imread("baby.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

### SOBEL EDGE DETECTOR

#### SOBEL X AXIS :
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

#### SOBEL Y AXIS :
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
#### SOBEL XY AXIS :
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

### LAPLACIAN EDGE DETECTOR
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

### CANNY EDGE DETECTOR
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
### SOBEL EDGE DETECTOR
#### SOBEL X AXIS:
![Screenshot from 2023-10-03 08-23-14](https://github.com/Gchethankumar/EDGEDETECTION/assets/118348224/8d5267ab-6353-4575-b4f5-57bec399839a)


#### SOBEL Y AXIS:
![Screenshot from 2023-10-03 08-23-25](https://github.com/Gchethankumar/EDGEDETECTION/assets/118348224/90d26ec0-fc91-46c5-b644-b85eaccf491c)


#### SOBEL XY AXIS:
![Screenshot from 2023-10-03 08-23-37](https://github.com/Gchethankumar/EDGEDETECTION/assets/118348224/ab76da3a-3d8b-4ab8-9adc-9f8eaa150467)


### LAPLACIAN EDGE DETECTOR
![Screenshot from 2023-10-03 08-23-44](https://github.com/Gchethankumar/EDGEDETECTION/assets/118348224/cd35309f-4c33-4faa-b14c-76797089c66d)



### CANNY EDGE DETECTOR
![Screenshot from 2023-10-03 08-23-51](https://github.com/Gchethankumar/EDGEDETECTION/assets/118348224/2c1043ae-21c2-40c0-8a41-dd3e796640f7)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
