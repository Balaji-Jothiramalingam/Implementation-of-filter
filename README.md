# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step 1:
Import necessary libraries: OpenCV, NumPy, and Matplotlib.Read an image, convert it to RGB format, define an 11x11 averaging kernel, and apply 2D convolution filtering.Display the original and filtered images side by side using Matplotlib.

## Step 2:
Define a weighted averaging kernel (kernel2) and apply 2D convolution filtering to the RGB image (image2).Display the resulting filtered image (image4) titled 'Weighted Averaging Filtered' using Matplotlib's imshow function.

## Step 3:
Apply Gaussian blur with a kernel size of 11x11 and standard deviation of 0 to the RGB image (image2).Display the resulting Gaussian-blurred image (gaussian_blur) titled 'Gaussian Blurring Filtered' using Matplotlib's imshow function.

## #Step 5:
Define a Laplacian kernel (kernel3) and perform 2D convolution filtering on the RGB image (image2).Display the resulting filtered image (image5) titled 'Laplacian Kernel' using Matplotlib's imshow function.

## Step 6:
Apply the Laplacian operator to the RGB image (image2) using OpenCV's cv2.Laplacian function.Display the resulting image (new_image) titled 'Laplacian Operator' using Matplotlib's imshow function.

## Program:
### Developed By   :balji J
### Register Number:212221243001


### 1. Smoothing Filters

i) Using Averaging Filter
```import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('/content/dipt.png')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

kernel = np.ones((11,11), np. float32)/121
image3 = cv2.filter2D(image2, -1, kernel)

plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('Orignal')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')




```
## ii) Using Weighted Averaging Filter
```

import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('/content/dipt.png')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image4 = cv2.filter2D(image2, -1, kernel2)
plt.imshow(image4)
plt.title('Weighted Averaging Filtered')



```
## iii) Using Gaussian Filter
```


import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('/content/dipt.png')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

gaussian_blur = cv2.GaussianBlur(src=image2, ksize=(11,11), sigmaX=0, sigmaY=0)
plt.imshow(gaussian_blur)
plt.title(' Gaussian Blurring Filtered')


```
## iv)Using Median Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('/content/dipt.png')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

median=cv2.medianBlur (src=image2, ksize=11)
plt.imshow(median)
plt.title(' Median Blurring Filtered')




```

### 2. Sharpening Filters
## i) Using Laplacian Linear Kernal
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('/content/dipt.png')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

kernel3 = np.array([[0,1,0], [1, -4,1],[0,1,0]])
image5 =cv2.filter2D(image2, -1, kernel3)
plt.imshow(image5)
plt.title('Laplacian Kernel')



```
## ii) Using Laplacian Operator
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('/content/dipt.png')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

new_image = cv2.Laplacian (image2, cv2.CV_64F)
plt.imshow(new_image)
plt.title('Laplacian Operator')



```

## OUTPUT:
### 1. Smoothing Filters

![314117218-e1402b4b-169e-4d6a-bd45-63e4b75e116a](https://github.com/user-attachments/assets/3bc9050d-343c-47ae-b16d-01b5a1e374e8)


## i) Using Averaging Filter

![314117492-21d4046c-0353-479c-8481-eadcab806cd2](https://github.com/user-attachments/assets/7d1ba8e7-f48e-4bd7-8048-3c1e68e0f70b)

## ii)Using Weighted Averaging Filter
![314118403-ebfc87b3-2f46-4f32-befe-5676c2064179](https://github.com/user-attachments/assets/89e6580d-9976-4aa5-af5e-73a608a5092e)


## iii)Using Gaussia
![314119847-f3e893ed-8bee-4574-a911-e2e7f5da5263](https://github.com/user-attachments/assets/a5fbc15f-0fde-4cf2-ac76-f4afcd482a0b)





## iv) Using Median Filter

![314121128-7c5cb227-9b47-4286-b4a0-6492127b4907](https://github.com/user-attachments/assets/c56e7319-daba-492f-8dde-338bf90322eb)



### 2. Sharpening Filters

## i) Using Laplacian Kernal

![314121491-7b06d5df-ec72-4b62-b950-3c4a9fb8e340](https://github.com/user-attachments/assets/ba79a677-c37f-47bd-b7c3-fc4d090b8ee4)

## ii) Using Laplacian Operator

![314121957-62ab2852-596a-4484-85ba-930d47a88772](https://github.com/user-attachments/assets/f0225fee-630a-43f6-90dd-183d699d1954)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
