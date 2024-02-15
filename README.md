# COLOR_CONVERSIONS_OF-IMAGE
## AIM:
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Google Colab
## Algorithm:
### Step1: Choose an image and save it as a filename.jpg ,
### Step2: Use imread(filename, flags) to read the file.
### Step3: Use imshow(window_name, image) to display the image.
### Step4: Use imwrite(filename, image) to write the image.
### Step5: End the program and close the output image windows.
### Step6: Convert BGR and RGB to HSV and GRAY
### Step7: Convert HSV to RGB and BGR
### Step8: Convert RGB and BGR to YCrCb
### Step9: Split and Merge RGB Image
### Step10: Split and merge HSV Image

## Program:
```
### Developed By: JEGADEESH S
### Register Number: 212222230055
```
<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
!pip install google-colab
from google.colab.patches import cv2_imshow

import cv2
color_image = cv2.imread('kk.png',1)
cv2_imshow(color_image)
cv2.waitKey(0)

``` 
  </td>
  <td>

### OUTPUT:
![image](https://github.com/JEGADEESH07/COLOR_CONVERSIONS_OF-IMAGE/assets/113497131/e66fc1c9-625a-421d-b2a9-3d3e5f060cff)


  </td>
  </tr>

   <tr>
    <td width=50%>

### ii)Write the image
```Python
    import cv2
    image=cv2.imread('kk.png',0)
    cv2.imwrite('d.jpg',image)
```
  </td>
  <td>

### OUTPUT:

![image](https://github.com/JEGADEESH07/COLOR_CONVERSIONS_OF-IMAGE/assets/113497131/9524004e-4612-43fb-8d84-97ab00decd31)


  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
    import cv2
    image=cv2.imread('kk.png',1)
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:
![image](https://github.com/JEGADEESH07/COLOR_CONVERSIONS_OF-IMAGE/assets/113497131/fbc1ad95-4963-4ab0-b729-337a10156ed9)

  </td>
  </tr>
  <tr>
    <td>
      
### iv)Access rows and columns
```Python
!pip install google-colab
from google.colab.patches import cv2_imshow
import random
import cv2
image=cv2.imread('kk.png',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
  for j in range(image.shape[1]):
    image[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)] 
cv2_imshow(image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

### OUTPUT:

![image](https://github.com/JEGADEESH07/COLOR_CONVERSIONS_OF-IMAGE/assets/113497131/6abcc11e-e3ba-4394-8cea-1f6b91068b9c)

  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v)Cut and paste portion of image

 ```Python
!pip install google-colab
from google.colab.patches import cv2_imshow
import cv2
import numpy as np
image=cv2.imread('kk.png',1)
image = cv2.resize(image, (400, 400))
print(image.shape)
tag =image[130:200,110:190]
image[110:180,120:200] = tag
cv2_imshow(image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
  </td>
  <td>
    
### OUTPUT:
![image](https://github.com/JEGADEESH07/COLOR_CONVERSIONS_OF-IMAGE/assets/113497131/25347a89-8d2c-442f-9744-ee7b472b2224)

  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
!pip install google-colab
from google.colab.patches import cv2_imshow
import cv2
img = cv2.imread('kk.png',1)
img = cv2.resize(img,(100,50))
cv2_imshow(img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2_imshow(hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2_imshow(hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2_imshow(gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2_imshow(gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![Untitled](https://github.com/JEGADEESH07/COLOR_CONVERSIONS_OF-IMAGE/assets/113497131/3bdf428c-1eea-4d2a-9dce-50cc404d8513)




### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('kk.png')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2_imshow(img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2_imshow(RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2_imshow(BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![Untitled](https://github.com/JEGADEESH07/COLOR_CONVERSIONS_OF-IMAGE/assets/113497131/a1667212-e22d-4bb0-9141-55aceadd709d)



### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('kk.png')
img = cv2.resize(img,(300,200))
cv2_imshow(img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2_imshow(YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2_imshow(YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![Untitled](https://github.com/JEGADEESH07/COLOR_CONVERSIONS_OF-IMAGE/assets/113497131/26019da9-b3e0-494f-995d-87532f57a293)




### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('kk.png',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2_imshow(R)
cv2_imshow(G)
cv2_imshow(B)
merged = cv2.merge((B,G,R))
cv2_imshow(merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![Untitled](https://github.com/JEGADEESH07/COLOR_CONVERSIONS_OF-IMAGE/assets/113497131/88badafb-b619-4f92-9726-90e9503c8c27)




### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("kk.png",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2_imshow(H)
cv2_imshow(S)
cv2_imshow(V)
merged = cv2.merge((H,S,V))
cv2_imshow(merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![Untitled](https://github.com/JEGADEESH07/COLOR_CONVERSIONS_OF-IMAGE/assets/113497131/09a7aac6-d771-40e5-9578-ac7621e1daa9)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







