
# OPENING--AND-CLOSING
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

 
## Program:
### DEVELOPED BY: Jenittan Jose J B
### REGISTER NO: 212224240063

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'Jenittan', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```


# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
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


<img width="699" height="174" alt="Screenshot 2025-11-12 222643" src="https://github.com/user-attachments/assets/5cb0a001-ce95-4027-aa48-f1541c356d24" />



### Display the result of Opening


<img width="727" height="173" alt="Screenshot 2025-11-12 222652" src="https://github.com/user-attachments/assets/c39185d8-e0eb-41da-ba17-731add2045c2" />



### Display the result of Closing

<img width="706" height="164" alt="Screenshot 2025-11-12 222701" src="https://github.com/user-attachments/assets/f2fb5b8a-10aa-4606-83e7-0e9bf4f0e9fc" />




## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
