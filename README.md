# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring element for opening and closing.

### Step4:
Apply erosion and dilation using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.

### Step5:
Show the images using cv2.imshow().
 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((300,500),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"MASK",(5,70),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation
img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Use Closing Operation
img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
 Developed by : A.Divya Mennakshi
 Register number : 212220230014

### Display the input Image
![image](https://user-images.githubusercontent.com/75235402/171097805-4ea7e989-ddd8-4aad-8d19-1874deddf11d.png)


### Display the result of Opening
![image](https://user-images.githubusercontent.com/75235402/171098032-1b481310-e79d-47e4-9baf-2856a4837b98.png)


### Display the result of Closing
![image](https://user-images.githubusercontent.com/75235402/171098081-4508f2c8-a23f-4b46-91e3-dec8c80d7198.png)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
