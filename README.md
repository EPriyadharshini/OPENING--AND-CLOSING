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

### OPENING
``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Engineer',(5,70), font,2,(255),5,cv2.LINE_AA)
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")

```
### CLOSING
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Engineer',(5,70), font,2,(255),5,cv2.LINE_AA)
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:

### Display the input Image
![image](https://github.com/YendluriChandana/OPENING--AND-CLOSING/assets/139842204/1825911b-0063-45dc-9ac0-9a1899015e42)


### Display the result of Opening
![image](https://github.com/YendluriChandana/OPENING--AND-CLOSING/assets/139842204/7e37d825-838e-453c-9271-1735036a7b17)



### Display the result of Closing
![image](https://github.com/YendluriChandana/OPENING--AND-CLOSING/assets/139842204/98f91498-6f3e-4cf7-aae9-4011375b4ffd)




## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
