# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages for implementing the code.
### Step2:
Create the text that you want to modify using opening and close filter.
### Step3:
Create the structuring element that you want to use over the image.
### Step4:
Apply the opening and closing operation for the original image.
### Step5:
Show the results using imshow function from cv2.
## Program:
~~~
DEVELOPED BY:G.Pavithra
REG NUMBER: 212221240036

# Import the necessary packages

import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX
im=cv2.putText(img1,' G.PAVITHRA ',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(im)

# Create the structuring element

Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation

image1=cv2.morphologyEx(im,cv2.MORPH_OPEN,Kernel)
plt.imshow(image1)


# Use Closing Operation

image1=cv2.morphologyEx(im,cv2.MORPH_CLOSE,Kernel)
plt.imshow(image1)
~~~
## Output:

### Display the input Image
![output](l1.png)
### Display the result of Opening
![output](l2.png)
### Display the result of Closing
![output](l3.png)
## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
