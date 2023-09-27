# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step 1:
Import the required packages for further process.

## Step 2:
Read the image and convert the bgr image to gray scale image.

## Step 3:
Use any filters for smoothing the image to reduse the noise.

## Step 4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

## Step 5:
Display the filtered image using plot and imshow.

## Program:
```
DEVELOPED BY :IYYANAR S
REF NO:212222240036

``` 
# Import the packages
```
import cv2
import matplotlib.pyplot as plt
```

# Load the image, Convert to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("night.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

# SOBEL EDGE DETECTOR

## SOBEL X AXIS:
```
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
## SOBEL Y AXIS:
```
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
## SOBEL XY AXIS:
```
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

# LAPLACIAN EDGE DETECTOR
```

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

# CANNY EDGE DETECTOR
```

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

## SOBEL X AXIS:
![71](https://github.com/Iyyanar22009120/EDGEDETECTION/assets/118680259/f0029960-b152-46b6-9e28-706ed0e5d864)

## SOBEL Y AXIS:
![72](https://github.com/Iyyanar22009120/EDGEDETECTION/assets/118680259/a7ff51f9-e226-4ccb-acbb-19e287b8842c)

## SOBEL XY AXIS:

![73](https://github.com/Iyyanar22009120/EDGEDETECTION/assets/118680259/c30baeba-66bf-4fe9-919a-67c70e7717f4)

### LAPLACIAN EDGE DETECTOR

![74](https://github.com/Iyyanar22009120/EDGEDETECTION/assets/118680259/13a33b0c-9822-4712-a01e-fca2c2e5f1f1)

### CANNY EDGE DETECTOR
![75](https://github.com/Iyyanar22009120/EDGEDETECTION/assets/118680259/d03b5b04-9e4b-463e-9b0e-36a452b48357)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors..
