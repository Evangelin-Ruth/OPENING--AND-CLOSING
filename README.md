# Opening-and-Closing

## AIM:
To implement Opening and Closing using Python and OpenCV.

## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV

## ALGORITHM:
### Step 1:
Import the necessary packages.

### Step 2:
Create the Text using cv2.putText.

### Step 3:
Create the structuring element.

### Step 4:
Use Opening operation.

### Step 5:
Use Closing Operation.

### Step 6:
Print the output and end the program.

 
## PROGRAM:

``` Python
# Import the necessary packages

import numpy as np
import matplotlib.pyplot as plt
import cv2

# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," Evangelin.S",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image)
plt.axis('off')

# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation

opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image)
plt.axis('off')

# Use Closing Operation

closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image)
plt.axis('off')
```
## OUTPUT:

### Display the input Image
![image](https://github.com/Evangelin-Ruth/OPENING--AND-CLOSING/assets/94219798/3b955344-409d-40f2-b004-f2bcd2e28904)
<br>

### Display the result of Opening
![image](https://github.com/Evangelin-Ruth/OPENING--AND-CLOSING/assets/94219798/1b92ca84-e501-43c9-871e-95ff8b7c6090)
<br>

### Display the result of Closing
![image](https://github.com/Evangelin-Ruth/OPENING--AND-CLOSING/assets/94219798/f65bf6cc-89e1-4a1e-a5c6-8e1d35cae467)
<br>

## RESULT:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
