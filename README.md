# Opening-and-Closing

## Aim:
To implement Opening and Closing using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the text image using cv2.putText.

### Step3:
Create the structuring element for opening and closing.

### Step4:
Use Opening and Closing Operations

### Step5:
End Program.

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((300,500),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"AD",(5,70),font,3,(255,0,0),5,cv2.LINE_AA)
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

### Display the input Image
![Original 31-05-2022 18_07_32](https://user-images.githubusercontent.com/75235386/171175545-d6b096e5-00c8-4bc9-b4e4-33dee2b1d878.png)

### Display the result of Opening
![Opening 31-05-2022 18_08_32](https://user-images.githubusercontent.com/75235386/171175600-4c1cd414-84f8-4c39-a209-87a68b9ebf20.png)

### Display the result of Closing
![Closing 31-05-2022 18_08_57](https://user-images.githubusercontent.com/75235386/171175641-95f05a5f-e7ea-4fdf-9807-e76be8bdf67d.png)

## Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
