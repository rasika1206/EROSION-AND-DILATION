# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

### Step1:
Import the necessary packages.

### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion.

### Step4:
Apply erosion and dilation using plt.erode and plt.dilate.

### Step5:
Plot the images using plt.imshow.
 
## Program:
```
Developed By:RASIKA.M
Register Number:212222230117
```

``` Python
# Import the necessary packages

import numpy as np
import cv2
import matplotlib.pyplot as plt
```
```
# Create the Text using cv2.putText

image = np.zeros((100,500),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image,"RASIKA",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(image,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()
```
```
# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
```
# Erode the image

image_erode=cv2.erode(image,kernel)
plt.imshow(image_erode,cmap='gray')
plt.title('Eroded Text'), plt.xticks([]), plt.yticks([])
plt.show()
```
```
# Dilate the image

image_dilate=cv2.dilate(image,kernel)
plt.imshow(image_dilate,cmap='gray')
plt.title('Dilated Text'), plt.xticks([]), plt.yticks([])
plt.show()
```



## Output:

### Display the input Image
<br>![Screenshot from 2023-10-23 10-05-46](https://github.com/rasika1206/EROSION-AND-DILATION/assets/124434806/13040324-4c6b-4203-a5e4-e840ec2aa96c)

<br>
<br>
<br>
<br>
<br>

### Display the Eroded Image
<br>![Screenshot from 2023-10-23 10-05-53](https://github.com/rasika1206/EROSION-AND-DILATION/assets/124434806/897caaa6-a7fe-4c2c-bb23-a729c4628719)

<br>
<br>
<br>
<br>
<br>

### Display the Dilated Image
<br>![Screenshot from 2023-10-23 10-11-53](https://github.com/rasika1206/EROSION-AND-DILATION/assets/124434806/3fd6110c-672a-42c2-8cf8-2fffbed71322)

<br>
<br>
<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
