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
### OPENING
``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'DataScience',(5,70), font,2,(255),5,cv2.LINE_AA)
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
cv2.putText(img1,'DataScience',(5,70), font,2,(255),5,cv2.LINE_AA)
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:

### Display the input Image
![Screenshot 2024-04-18 000649](https://github.com/abinayasangeetha/OPENING--AND-CLOSING/assets/119393675/f7f3f2b5-1fe7-40fd-836b-80a2160e1e6c)


### Display the result of Opening
![Screenshot 2024-04-18 000649](https://github.com/abinayasangeetha/OPENING--AND-CLOSING/assets/119393675/3a12158f-41f5-453c-8eba-24b4e265a402)

### Display the result of Closing
![Screenshot 2024-04-18 000656](https://github.com/abinayasangeetha/OPENING--AND-CLOSING/assets/119393675/2f180066-a553-400b-a604-d63fc5ffca8f)



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
