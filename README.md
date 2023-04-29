# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step1:
Import the necessary packages to do Erosion and Dilution.

## Step2:
Create the text image of our name using putText from cv2 package.

## Step3:
Create the required structural element.

## Step4:
Apply Erode and Dilution for our NameImage.

## Step5:
Display the output images.

## step6:
End the programm
 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
image= np.zeros((100,600),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image,'SK SAMEER BASHA',(5,70), font,2,(255),5,cv2.LINE_AA)
cv2.imshow("Name",image)

# Create the structuring element
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
erodeImage = cv2.erode(image,kernel1)
cv2.imshow("Erode Image",erodeImage)

# Dilate the image
dilationImage = cv2.dilate(image,kernel1)
cv2.imshow("Dilated Image",dilationImage)

cv2.waitKey(0)
cv2.destoryAllWindows
```
## Output:

### Display the input Image
![Screenshot from 2023-04-29 10-49-02](https://user-images.githubusercontent.com/118707756/235286236-f7ed3891-34f4-46b6-b43e-b6b8ea89047b.png)
### Display the Eroded Image
![Screenshot from 2023-04-29 10-58-57](https://user-images.githubusercontent.com/118707756/235286249-d97c8135-41a7-4011-b8ae-494658d331cc.png)

### Display the Dilated Image
![Screenshot from 2023-04-29 11-00-43](https://user-images.githubusercontent.com/118707756/235286339-f1f409d9-4656-4b58-9884-2504c6e9d31e.png)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
