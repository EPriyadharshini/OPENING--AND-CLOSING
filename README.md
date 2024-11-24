# OPENING--AND-CLOSING

## Aim

To implement Opening and Closing using Python and OpenCV.

## Software Required

1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:

### Step1:
<br>Import the necessary packages


### Step2:
<br>Create the Text using cv2.putText

### Step3:
<br>Create the structuring element

### Step4:
<br>Use Opening operation

### Step5:
<br>Use Closing Operation

 
## Program:
## NAME: PRIYADHARSHINI E
## REG NO :212223230159

```
### text input

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 1: Create a blank image
image = np.zeros((300, 600, 3), dtype="uint8")

# Step 2: Create the text using cv2.putText
text = " Demo"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)

# Step 3: Create a structuring element (5x5 rectangular)
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# Step 4: Use Opening operation (erosion followed by dilation)
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# Step 5: Use Closing operation (dilation followed by erosion)
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

# Convert images from BGR to RGB for Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)

# Plot the original, opening, and closing images using Matplotlib
plt.figure(figsize=(10, 5))

plt.subplot(1, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 3, 2)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")

plt.subplot(1, 3, 3)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")

plt.tight_layout()
plt.show()


```


### image input
  ```

import cv2
import matplotlib.pyplot as plt
import numpy as np
# Step 1: Load the image using cv2.imread()
image = cv2.imread("img.png")  # Make sure the file path is correct

# Step 2: Create a structuring element (5x5 rectangular)
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# Step 3: Use Opening operation (erosion followed by dilation)
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# Step 4: Use Closing operation (dilation followed by erosion)
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

# Convert images from BGR to RGB for Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)

# Plot the original, opening, and closing images using Matplotlib
plt.figure(figsize=(10, 5))


plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")


plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")

plt.subplot(1, 3, 3)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")

plt.tight_layout()
plt.show()

  ```




# output



text- input 


    ![image](https://github.com/user-attachments/assets/61658fcc-b4ab-4137-ad53-436d26f4b21c)


image -input


   ![image](https://github.com/user-attachments/assets/ca3075e7-a27d-4c21-81ae-8390c7f373a4)




## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
