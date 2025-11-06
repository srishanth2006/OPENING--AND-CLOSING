# OPENING--AND-CLOSING
# Developed By: SRISHANTH J
# Reg no: 212223240160
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation
 
## Program:

``` Python
# Developed By: Daniel C
# reg no: 212223240023
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 1: Load the image using cv2.imread()
image = cv2.imread("Fish.jpg")  

# Step 2: Create a structuring element (5x5 rectangular)
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# Plot the original, opening, and closing images using Matplotlib
plt.figure(figsize=(10, 5))

plt.subplot(1, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")



# Use Opening operation
# Step 3: Use Opening operation (erosion followed by dilation)
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)

plt.subplot(1, 3, 2)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")



# Use Closing Operation
# Step 4: Use Closing operation (dilation followed by erosion)
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
# Convert images from BGR to RGB for Matplotlib
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)
plt.subplot(1, 3, 3)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")

plt.tight_layout()
plt.show()





```
## Output:

### Display the input Image
<img width="483" height="333" alt="image" src="https://github.com/user-attachments/assets/1855cf87-1454-444c-8457-bbe0fc0f1956" />


### Display the result of Opening
<img width="488" height="346" alt="image" src="https://github.com/user-attachments/assets/e8c30d8d-04ff-4a5e-8e9a-827698e2892a" />


### Display the result of Closing
<img width="503" height="345" alt="image" src="https://github.com/user-attachments/assets/35bb4282-f8c4-4dde-952f-4c7b1a14e053" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
