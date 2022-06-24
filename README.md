### EX NO : 05
### DATE  : 30.04.2022
# <p align="center">Rotating the Gaming Object</p>
# Image-Transformation
## AIM:
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step 1:
Import the necessary libraries and read the original image and save it as a image variable.
### Step 2:
Translate the image using<br>
M=np.float32([[1,0,20],[0,1,50],[0,0,1]])<br>
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
### Step 3:
Scale the image using<br>
M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]])<br>
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
### Step 4:
Shear the image using<br>
M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]])<br>
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
### Step 5:
Reflection of image can be achieved through the code<br>
M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])<br>
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
### Step 6:
Rotate the image using<br>
angle=np.radians(45)<br>
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])<br>
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
### Step 7:
Crop the image using <br>
cropped_img=input_img[20:150,60:230]
### Step 8:
Display all the Transformed images.
## PROGRAM:
```python
Developed By: Vijayaragavan ARR
Register Number: 212220230059
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("img.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
i)Image Translation
M=np.float32([[1,0,20],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()

ii) Image Scaling
M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()

iii)Image shearing
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()

iv)Image Reflection
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()

v)Image Rotation
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()

vi)Image Cropping
cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()

```
## Output:
### i)Image Translation
![output](https://user-images.githubusercontent.com/75235488/166113460-249d85d2-6b7e-4809-b3f2-2086a8385f9a.png)


### ii) Image Scaling
![output1](https://user-images.githubusercontent.com/75235488/166113483-14829160-35ed-42f1-9c49-81c8015493c7.png)


### iii)Image shearing
![output2](https://user-images.githubusercontent.com/75235488/166113498-0a9c34a6-9710-44ec-b70c-1e0680804023.png)
![output3](https://user-images.githubusercontent.com/75235488/166113504-5c71606e-0f6e-464b-aa62-7e91028ec03e.png)


### iv)Image Reflection
![output4](https://user-images.githubusercontent.com/75235488/166113510-8b7be8f3-d2d4-4285-b536-390372127e6e.png)
![output5](https://user-images.githubusercontent.com/75235488/166113511-7e341173-13bb-4c40-becb-ea0d974f9bbe.png)


### v)Image Rotation
![output 6](https://user-images.githubusercontent.com/75235488/166113519-f5e16e18-b20c-41bd-ade7-b3059636b1a6.png)


### vi)Image Cropping
![output 7](https://user-images.githubusercontent.com/75235488/166113525-c9979664-1ac2-4791-b5d2-2f362f3244d2.png)


## RESULT: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
