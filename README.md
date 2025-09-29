# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1

Import the required libraries.

### Step2

Convert the image from BGR to RGB.

### Step3

Apply the required filters for the image separately.

### Step4

Plot the original and filtered image by using matplotlib.pyplot.

### Step5

End the program.


## Program:

### Developed By   :  NITHEESH YEGAVINTI
### Register Number:  212224040370
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("C:\\Users\\admin\\Downloads\\palm tree.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()

```

ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()

```

iii) Using Gaussian Filter
```

gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()


```

iv)Using Median Filter

```

median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()


```

### 2. Sharpening Filters

i) Using Laplacian Linear Kernal

```


kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()



```
ii) Using Laplacian Operator

```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()

```

## OUTPUT:
## Smoothing Filters

i) Using Averaging Filter

<img width="1103" height="312" alt="image" src="https://github.com/user-attachments/assets/d2a98436-a180-4df0-89a8-f184a4e0a22f" />


ii)Using Weighted Averaging Filter

<img width="796" height="252" alt="image" src="https://github.com/user-attachments/assets/89e4abea-363d-4c52-b051-2f97abc11426" />


iii)Using Gaussian Filter

<img width="732" height="252" alt="image" src="https://github.com/user-attachments/assets/6bda8619-5730-4bda-bc76-35e5ce140b5c" />



iv) Using Median Filter


<img width="977" height="305" alt="image" src="https://github.com/user-attachments/assets/fce9cf79-e6ba-4981-82c2-d47f7f1e8d46" />


### 2. Sharpening Filters


i) Using Laplacian Kernal

<img width="802" height="246" alt="image" src="https://github.com/user-attachments/assets/9d9f0454-5b44-4543-9e3b-55494a457a9e" />


ii) Using Laplacian Operator

<img width="806" height="242" alt="image" src="https://github.com/user-attachments/assets/3c8f74a0-2f93-460a-ae64-0b293d1f30e1" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
