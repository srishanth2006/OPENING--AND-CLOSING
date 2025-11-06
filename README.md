# Ex 10 OPENING--AND-CLOSING
# Name : ALDRIN.S
# Reg no : 212223240005

## Aim
To implement Opening and Closing using Python and OpenCV.

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
Use Opening operation.

### Step5:
Use Closing Operation.

 
## Program
# Import the necessary packages
```
Developed by : SRISHANTH J
Reg no : 212223240160

import cv2
import numpy as np
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'Ayisha Rinsi K', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```


# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11)
```
# Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")

```
# Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")



```
## Output:

### Display the input Image

<img width="723" height="194" alt="image" src="https://github.com/user-attachments/assets/1f3dd088-66f6-41ca-9677-96c1646d3344" />


### Display the result of Opening
<img width="706" height="177" alt="image" src="https://github.com/user-attachments/assets/c7ab8125-1fa6-4288-8cdb-b289d1a5914c" />



### Display the result of Closing
<img width="704" height="210" alt="image" src="https://github.com/user-attachments/assets/6f3eebf0-c008-41f8-b9e6-4d0c0481304a" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
