# IMAGE-TRANSFORMATIONS

## NAME: Rhudhra phriyamvadha K S
## REG NO: 212224040275

## Aim:
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import necessary libraries such as OpenCV, NumPy, and Matplotlib for image processing and visualization.

### Step2:
Read the input image using cv2.imread() and store it in a variable for further processing.

### Step3:
Apply various transformations like translation, scaling, shearing, reflection, rotation, and cropping by defining corresponding functions:

1.Translation moves the image along the x or y-axis.

2.Scaling resizes the image by scaling factors.

3.Shearing distorts the image along one axis.

4.Reflection flips the image horizontally or vertically.

5.Rotation rotates the image by a given angle.

### Step4:
Display the transformed images using Matplotlib for visualization. Convert the BGR image to RGB format to ensure proper color representation.


## Program:
```python

Developed By: Rhudhra phriyamvadha K S
Register Number: 212224040275
```
### i)Original image:
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image=cv2.imread("Image1.jpg")
image.shape
#Display the images.
plt.imshow(image[:,:,::-1])
plt.title("Original Image")
plt.show()
```
### Output:


<img width="450" height="501" alt="image" src="https://github.com/user-attachments/assets/832f7777-9381-463f-8d06-73436c67fbd8" />


### ii) Image Translation:
```python
tx,ty=100,200
M_translation=np.float32([[1,0,tx],[0,1,ty]])
translated_image=cv2.warpAffine(image,M_translation, (673,419))
plt.imshow(translated_image[:,:,::-1])
plt.title("Translated Image")
plt.axis("on")
plt.show()
```
### Output:

<img width="654" height="435" alt="Screenshot 2025-09-08 212225" src="https://github.com/user-attachments/assets/cf09e772-c992-46f0-b894-c1379509c338" />


### iii)Image scaling:
```python
fx, fy = 5.0, 2.0  
scaled_image = cv2.resize(image, None, fx=fx, fy=fy, interpolation=cv2.INTER_LINEAR)

plt.imshow(cv2.cvtColor(scaled_image, cv2.COLOR_BGR2RGB))  
plt.title("Scaled Image")  # Set title
plt.axis('off')
```
### Output:

<img width="665" height="358" alt="image" src="https://github.com/user-attachments/assets/8f8214a4-d512-4aec-b46d-e8904ab7dfbb" />


### iv)Image Shearing:
```python
shear_matrix = np.float32([[1, 0.5, 0], [0.5, 1, 0]])
sheared_image = cv2.warpAffine(image, shear_matrix, (image.shape[1], image.shape[0]))

plt.imshow(cv2.cvtColor(sheared_image, cv2.COLOR_BGR2RGB))  
plt.title("Sheared Image")  
plt.axis('off')
```
### Output:

<img width="667" height="500" alt="image" src="https://github.com/user-attachments/assets/a4c59cfd-0db8-4ea6-9fc6-49ea12789cd7" />


### v)Image Reflection:
```python
reflected_image = cv2.flip(image, 2)

plt.imshow(cv2.cvtColor(reflected_image, cv2.COLOR_BGR2RGB))  
plt.title("Reflected Image")  
plt.axis('off')
```
### Output:


<img width="662" height="498" alt="image" src="https://github.com/user-attachments/assets/5476d30c-3f2d-4f8c-aa77-96967dd8b50b" />


### vi)Image Rotation:
```python
(height, width) = image.shape[:2] 
angle = 45 
center = (width // 2, height // 2)  
M_rotation = cv2.getRotationMatrix2D(center, angle, 1)
rotated_image = cv2.warpAffine(image, M_rotation, (width, height))

plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Rotated Image")  
plt.axis('off')
```
### Output:

<img width="702" height="500" alt="image" src="https://github.com/user-attachments/assets/ba62c893-639f-4827-ad42-94f7ebe24103" />


### vii)Image Cropping:
```python
x, y, w, h = 100, 100, 200, 150 
cropped_image = image[y:y+h, x:x+w]

plt.imshow(cv2.cvtColor(cropped_image, cv2.COLOR_BGR2RGB)) 
plt.title("Cropped Image")  
plt.axis('off')

```

### Output:


<img width="648" height="502" alt="image" src="https://github.com/user-attachments/assets/2067fa8d-e3f9-4a4a-95d6-ebd9bbe1e42a" />


## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
