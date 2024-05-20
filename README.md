# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step1:
Import the necessary pacakages

## Step2:
Create the text using cv2.putText

## Step3:
Create the structuring element

## Step4:
Erode the image

## Program:
```
Import the necessary packages

import numpy as np
import cv2
import matplotlib.pyplot as plt

Create the Text using cv2.putText
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'Lifestyle',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')

Create the structuring element
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)

Erode the image
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

Dilate the image
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```

## Output:

### Display the input Image
![image](https://github.com/MANOKARTHICK09/erosion--dilation/assets/121785458/8d14f2f3-7ced-4941-88d6-36936b9367ce)
![image](https://github.com/MANOKARTHICK09/erosion--dilation/assets/121785458/8d14f2f3-7ced-4941-88d6-36936b9367ce)


### Display the Eroded Image
![image](https://github.com/MANOKARTHICK09/erosion--dilation/assets/121785458/475aa945-6ba3-453e-8072-aeb017541a2d)
![image](https://github.com/MANOKARTHICK09/erosion--dilation/assets/121785458/475aa945-6ba3-453e-8072-aeb017541a2d)


### Display the Dilated Image
![image](https://github.com/MANOKARTHICK09/erosion--dilation/assets/121785458/81b918a6-fc63-4709-9627-7d7b8bad9a6a)
![image](https://github.com/MANOKARTHICK09/erosion--dilation/assets/121785458/81b918a6-fc63-4709-9627-7d7b8bad9a6a)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
