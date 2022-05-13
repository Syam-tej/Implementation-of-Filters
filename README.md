# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1 :- 
Import the required modules.


## Step2 :- 
Convert the image from BGR to RGB.


## Step3:- 
Apply the required filters for the image separately.


## Step4:- 
Plot the original and filtered image by using matplotlib.pyplot


## Step5:- 
End the program.


## Program:
### Developed By   :P.SYAM TEJ
### Register Number:212221240056
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("bike.jpeg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)

kernel1 = np.ones((11,11),np.float32)/121
avg_filter = cv2.filter2D(original_image,-1,kernel1)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(avg_filter)
plt.title("Filtered")
plt.axis("off")




```
ii) Using Weighted Averaging Filter
```
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weighted_filter = cv2.filter2D(original_image,-1,kernel2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(weighted_filter)
plt.title("Filtered")
plt.axis("off")





```
iii) Using Gaussian Filter
```
gaussian_blur = cv2.GaussianBlur(src = original_image, ksize = (11,11), sigmaX=0, sigmaY=0)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Filtered")
plt.axis("off")





```

iv) Using Median Filter
```
median = cv2.medianBlur(src=original_image,ksize = 11)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Filtered")
plt.axis("off")




```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_kernel)
plt.title("Filtered")
plt.axis("off")




```
ii) Using Laplacian Operator
```
laplacian_operator = cv2.Laplacian(original_image,cv2.CV_64F)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_operator)
plt.title("Filtered")
plt.axis("off")




```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
![d1](https://user-images.githubusercontent.com/93427224/168208146-6ec30c2f-d095-4e52-afdd-443fb82395c1.png)


ii) Using Weighted Averaging Filter
![d2](https://user-images.githubusercontent.com/93427224/168208293-f40d44a6-34a8-44c4-abb9-ffa8c7801b50.png)

iii) Using Weighted Averaging Filter
![d3](https://user-images.githubusercontent.com/93427224/168208278-94f2311d-b64f-4717-8eb8-2ef5da56ead8.png)

iv) Using Median Filter
![d4](https://user-images.githubusercontent.com/93427224/168208266-d07aa5c3-8594-4356-a4a0-afb987bf57fc.png)


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
![d5](https://user-images.githubusercontent.com/93427224/168208335-8e84b585-7c46-452b-a47c-b7ba8c056f11.png)


ii) Using Laplacian Operator
![d6](https://user-images.githubusercontent.com/93427224/168208356-23d1dbc7-06a4-406c-89ec-e001cf57e672.png)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
