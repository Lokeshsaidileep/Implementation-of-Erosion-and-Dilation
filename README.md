# Implementation-of-Erosion-and-Dilation

## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Erode the image using cv2.erode().

### Step5:
Dilate the image using cv2.dilate().

 
## Program:

```python

# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt
# Load the Image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
# Create the Text using cv2.putText
cv2.putText(img1,'LOKESH SAI DILEEP',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')
# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
# Erode the image
img_erode=cv2.erode(img1,kernel1)
plt.imshow(img_erode,cmap='gray')

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
plt.imshow(img_dilate,cmap='gray')


```
## Output:

### Display the input Image
![image](https://user-images.githubusercontent.com/94883079/235294741-29c958ab-5d93-452c-bf8e-fa48cd64a990.png)

### Display the Eroded Image

![image](https://user-images.githubusercontent.com/94883079/235294752-ea9f4970-cfc8-45c6-8a41-e787e3ed89d5.png)

### Display the Dilated Image
![image](https://user-images.githubusercontent.com/94883079/235294810-ad6b6db3-e043-4814-a2cf-3cf9db8c6c6c.png)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
