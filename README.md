# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required libraries and read the original image.

### Step2:
Translate the image.

### Step3:
Scale the image.

### Step4:
Shear the image.

### Step5:
Find reflection of image.

### Step 6:
Rotate the image.

### Step 7:
Crop the image.

### Step 8:
Display all the Transformed images.

## Program:
```
Developed By: LOGESHWARI.P
Register Number: 212221230055

import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("gate (1).jpg")
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()

i)Image Translation
rows, cols, dim=input_image.shape
M=np.float32([[1, 0, 100],
              [0, 1, 200],
              [0, 0, 1]])
translated_image=cv2.warpPerspective(input_image, M, (cols, rows))

plt.axis('off')
plt.imshow(translated_image)
plt.show()

ii) Image Scaling
rows, cols, dim =input_image.shape
M=np.float32([[1.5, 0,   0],
              [0,   1.8, 0],
              [0,   0,   1]])
scaled_image=cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_image)
plt.show()

iii)Image shearing
M_x=np.float32([[1, 0.5, 0],
                [0, 1, 0],
                [0, 0, 1]])
M_y=np.float32([[1, 0, 0],
                [0.5, 1, 0],
                [0, 0, 1]])
sheared_image_xaxis= cv2.warpPerspective(input_image,M_x,(int(cols*1.5),int(rows*1.5)))
sheared_image_yaxis= cv2.warpPerspective(input_image,M_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_image_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_image_yaxis)
plt.show()

iv)Image Reflection
rows, cols, dim = input_image.shape
M_x=np.float32([[1, 0, 0],
                [0, -1, rows],
                [0, 0, 1]])
M_y=np.float32([[-1, 0, cols],
                [0, 1, 0],
                [0, 0, 1]])
reflected_image_xaxis= cv2.warpPerspective(input_image,M_x,(int(cols),int(rows)))
reflected_image_yaxis= cv2.warpPerspective(input_image,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_image_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_image_yaxis)
plt.show()

v)Image Rotation
angle=np.radians(10)
M=np.float32([[np.cos(angle), -(np.sin(angle)), 0],
              [np.sin(angle), np.cos(angle), 0],
              [0, 0, 1]])
rotated_img=cv2.warpPerspective(input_image, M, (int(cols), int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()

vi)Image Cropping
cropped_img=input_image[100:300,100:300]
plt.axis("off")
plt.imshow(cropped_img)
plt.show()





```
## Output:

![230605945-0192c116-ef60-438e-9e30-ce002f6c2324](https://user-images.githubusercontent.com/94211349/232268567-5f3e65a1-5737-418a-b10c-f00acce7a77a.png)

### i)Image Translation
![230606009-62920550-cfab-489d-aea3-876d89d85ccb](https://user-images.githubusercontent.com/94211349/232268728-dcd0904d-146a-470d-95aa-0be16806648f.png)


### ii) Image Scaling
![230606092-bc245a47-6282-4324-adb9-c96718048e0e](https://user-images.githubusercontent.com/94211349/232268808-d0bc4552-19d4-411c-9c09-4f6ce10de07d.png)

### iii)Image shearing
![230606123-de79a47a-b6ff-4c0a-af2f-d16a0653f558](https://user-images.githubusercontent.com/94211349/232268896-005b853b-d838-4423-9d03-22c31f9e3af3.png)

### iv)Image Reflection
![230606168-3f331813-25dd-476c-b7c7-66302471bc5a](https://user-images.githubusercontent.com/94211349/232269007-dfc9b734-919e-49b6-8a04-514dab6374d0.png)

### v)Image Rotation
![230606201-6ddc6a74-6398-451e-a842-956bde27e859](https://user-images.githubusercontent.com/94211349/232269147-3ff355d6-e800-4daf-bb55-3c0bdfcae990.png)

### vi)Image Cropping
![230606242-f75e288e-1f22-46b1-a70a-ec4f92ec6edd](https://user-images.githubusercontent.com/94211349/232269277-6f49904c-a5f6-4e02-aca3-592d0752c5ca.png)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
