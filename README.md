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
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion.

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:
Plot the images using plt.imshow.
 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," Harshini ",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')


# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image

image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'magma')
plt.axis('off')

# Dilate the image

image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'magma')
plt.axis('off')
```
## Output:

### Display the input Image
<img width="282" alt="image" src="https://user-images.githubusercontent.com/75235554/170839709-1ac3f425-6f4e-4f54-93e6-cfc2530350d0.png">

### Display the Eroded Image
<img width="276" alt="image" src="https://user-images.githubusercontent.com/75235554/170839729-ed6bbeb8-6d59-4730-842e-62a20883ce4d.png">

### Display the Dilated Image
<img width="297" alt="image" src="https://user-images.githubusercontent.com/75235554/170839736-0566b078-9888-4b50-9b6d-aa940aeb2af6.png">

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
