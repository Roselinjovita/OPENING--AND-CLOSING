# OPENING--AND-CLOSING
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

 
## Program and Output:

```
Developed by : Roselin mary jovita s
Reg no : 212222230122
```

### Import the necessary packages
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

### Read and display the original image
```p
image = cv2.imread("fingerprint.jpg")
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```

![Screenshot 2024-10-26 114403](https://github.com/user-attachments/assets/85182032-da35-415a-bca3-20fb5e608366)


### Create the structuring element
```p
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
```

### Use Opening operation
```p
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")
```
![Screenshot 2024-10-26 114410](https://github.com/user-attachments/assets/4d9686cd-4a53-4419-af2d-57e47f919ccd)



### Use Closing Operation
```p
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")
plt.tight_layout()
plt.show()
```

![Screenshot 2024-10-26 114417](https://github.com/user-attachments/assets/8fc4f8ce-af34-4d08-b258-d1997966e6c7)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
