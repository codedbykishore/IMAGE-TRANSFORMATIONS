# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import necessary libraries such as OpenCV, NumPy, and Matplotlib for image processing and visualization.
<br>

### Step2:
<br>
Read the input image using cv2.imread() and store it in a variable for further processing.

### Step3:
<br>
Apply various transformations like translation, scaling, shearing, reflection, rotation, and cropping by defining corresponding functions:

1.Translation moves the image along the x or y-axis. 2.Scaling resizes the image by scaling factors. 3.Shearing distorts the image along one axis. 4.Reflection flips the image horizontally or vertically. 5.Rotation rotates the image by a given angle.

### Step4:
<br>
Display the transformed images using Matplotlib for visualization. Convert the BGR image to RGB format to ensure proper color representation.

### Step5:
<br>
Save or display the final transformed images for analysis and use plt.show() to display them inline in Jupyter or compatible environments.


Developed By: KISHORE B
Register Number:212223240073


## Program:


# Function to display image using Matplotlib
```
import cv2
import numpy as np
```
# Load the image
```
image = cv2.imread('boy.jpg') # Replace with your image path
(h, w) = image.shape[:2]
```

# i) Image Translation
# Move image 100 pixels right and 50 pixels down
```
tx, ty = 100, 50
translation_matrix = np.float32([[1, 0, tx], [0, 1, ty]])
translated = cv2.warpAffine(image, translation_matrix, (w, h))
```

# iii) Image Shearing
```
# Shear image horizontally
shear_matrix = np.float32([[1, 0.5, 0], [0, 1, 0]]) # x-shear
sheared = cv2.warpAffine(image, shear_matrix, (int(w + 0.5*h), h))
```

# iv) Image Reflection
# Flip horizontally (mirror image)
```
h_flip = cv2.flip(image, 1)
```
# Flip vertically
```
24
v_flip = cv2.flip(image, 0)
```
# v) Image Rotation
# Rotate by 45 degrees around the center
```
angle = 45
scale = 1.0
center = (w // 2, h // 2)
rotation_matrix = cv2.getRotationMatrix2D(center, angle, scale)
rotated = cv2.warpAffine(image, rotation_matrix, (w, h))

# vi) Image Cropping

# Crop a region (top-left 200x200)
cropped = image[0:200, 0:200]


```
## Output:

![exp4op1](https://github.com/user-attachments/assets/dea7ec18-5928-421e-a002-2fd03948dbaf)

### i)Image Translation

![exp4op2](https://github.com/user-attachments/assets/0b7cbd74-750e-447d-8f2b-14162f3c599d)



### ii) Image Scaling

![exp4op4](https://github.com/user-attachments/assets/56372419-8e28-442f-850e-fff9fb9a7137)




### iii)Image shearing

![exp4op3](https://github.com/user-attachments/assets/6e5f0368-bcab-4402-bcfa-0b805e81afca)




### iv)Image Reflection


![exp4op5](https://github.com/user-attachments/assets/16af11ea-98b8-491c-8849-9779a7b9a569)


![exp4op6](https://github.com/user-attachments/assets/be9777a2-ccfe-476f-8f80-89c90df83fca)




### v)Image Rotation
![exp4op7](https://github.com/user-attachments/assets/f69dcb67-3384-4c52-90de-c47e3de2af72)



### vi)Image Cropping
![exp4op8](https://github.com/user-attachments/assets/12a4be72-93eb-4d28-be92-f4a8c69586af)






## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
