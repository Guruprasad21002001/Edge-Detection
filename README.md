# Edge-Detection...

## Aim:

To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:

Anaconda - Python 3.7 

## Algorithm:

### Step1:

Import the required packages for further process.

### Step2:

Read the image and convert the bgr image to gray scale image.

### Step3:

Use any filters for smoothing the image to reduse the noise.

### Step4:

Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step5:

Display the filtered image using plot and imshow.
 
 
## Program:

```python 

# Import the packages and load the image, Convert to grayscale and remove noise

import cv2
import matplotlib.pyplot as plt
image = cv2.imread("must.jpeg")
plt.imshow(image)
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)

# SOBEL EDGE DETECTOR:

# SOBEL-X:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("must.jpeg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel-X")
plt.xticks([])
plt.yticks([])
plt.show()

# SOBEL-Y:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("must.jpeg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel-Y")
plt.xticks([])
plt.yticks([])
plt.show()

# SOBEL-XY:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("must.jpeg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelxy=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel-XY")
plt.xticks([])
plt.yticks([])
plt.show()

# LAPLACIAN EDGE DETECTOR:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("must.jpeg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
laplacian = cv2.Laplacian(img,cv2.CV_64F)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='Blues')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap='Blues')
plt.title("Laplacian")
plt.xticks([])
plt.yticks([])
plt.show()

# CANNY EDGE DETECTOR:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("must.jpeg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
canny_edges = cv2.Canny(image, 120, 150)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(canny_edges,cmap='gray')
plt.title("Canny_edges")
plt.xticks([])
plt.yticks([])
plt.show()

```

## Output:

### INPUT IMAGE:

![img1](https://user-images.githubusercontent.com/95342910/232320146-cbde7a6d-84ac-4106-879f-852ade4f2723.png)


### SOBEL EDGE DETECTOR:

### SOBEL-X:

![img2](https://user-images.githubusercontent.com/95342910/232320152-a4ab26c0-95cf-46cb-affb-e93b7f467460.png)


### SOBEL-Y:

![img3](https://user-images.githubusercontent.com/95342910/232320155-1c305f65-f54b-4df7-8354-c4b021b1e372.png)


### SOBEL-XY:


![img4](https://user-images.githubusercontent.com/95342910/232320166-4d166c92-1887-4b1f-9fbe-82e1db48caa4.png)

### LAPLACIAN EDGE DETECTOR:

![img5](https://user-images.githubusercontent.com/95342910/232320167-065bf243-b23d-47da-992f-46f1605a840a.png)


### CANNY EDGE DETECTOR:


![img6](https://user-images.githubusercontent.com/95342910/232320184-99973ddc-9b71-4936-ad80-1f47534589d2.png)

## Result:

Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.


