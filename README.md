# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1
Import the required libraries.


### Step2
Read the image by using imread().


### Step3
Apply the required filters for the image separately.


### Step4
Plot the original and filtered image by using matplotlib.pyplot.


### Step5
End the program.

## Program:
### Developed By : K SANTHAN KUMAR
### Register Number : 212223240065
</br>

### 1. Smoothing Filters

 ### i) Using Averaging Filter
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("lucid 3.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernal = np.ones((11,11),np.float32)/121
img2 = cv2.filter2D(img1,-1,kernal)

plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(img2)
plt.title('Filtered')
plt.axis('off')

```
## OUTPUT :
![image](https://github.com/SANTHAN-2006/Implementation-of-filter/assets/80164014/39b2b66f-e6e8-469a-9c50-47f9c3845ad8)

### ii) Using Weighted Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("lucid 3.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernal2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
img2 = cv2.filter2D(img1,-1,kernal2)

plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(img2)
plt.title('Filtered')
plt.axis('off')

```
## OUTPUT :
![image](https://github.com/SANTHAN-2006/Implementation-of-filter/assets/80164014/42546d20-08a9-4091-a632-9ecbe208cdf3)

### iii) Using Gaussian Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("luicd 3.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
gaussian_blur =  cv2.GaussianBlur(src=img1,ksize=(11,11),sigmaX=0,sigmaY=0)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title('Filtered')
plt.axis('off')

```
## OUTPUT :
![image](https://github.com/SANTHAN-2006/Implementation-of-filter/assets/80164014/83ee62f3-7e24-4615-8cb1-2d8aef327fa9)

### iv) Using Median Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("lucid 3.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
median = cv2.medianBlur(src=img1,ksize=11)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(median)
plt.title('Filtered')
plt.axis('off')

```
## OUTPUT :
![image](https://github.com/SANTHAN-2006/Implementation-of-filter/assets/80164014/165dda57-d158-4e2d-8cbd-cae43bb563e2)

### 2. Sharpening Filters
### i) Using Laplacian Kernal
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("lucid 3.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernal3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
img3 = cv2.filter2D(img1,-1,kernal3)

plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(img3)
plt.title('Filtered')
plt.axis('off')

```
## OUTPUT :
![image](https://github.com/SANTHAN-2006/Implementation-of-filter/assets/80164014/49e67ced-6123-48b0-8a24-70cb376207cc)

### ii) Using Laplacian Operator
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("lucid 3.jpg")
img1 = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernal3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
img3 = cv2.filter2D(img1,-1,kernal3)
new_img = cv2.Laplacian(img1,cv2.CV_64F)

plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(new_img)
plt.title('Filtered')
plt.axis('off')

```
## OUTPUT :
![image](https://github.com/SANTHAN-2006/Implementation-of-filter/assets/80164014/d0c6fa7b-cec9-461a-94a9-9ee2c72c7645)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
