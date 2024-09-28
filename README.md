# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()
### Step2:
Print the image using imshow().
### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.
### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.
### Step5:
The Histogram of gray scale image and color image is shown.

## Program:
### Developed By: kathiravan p
### Register Number: 212222230063
### Input Grayscale Image and Color Image
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('photo1.jpeg')
color_image = cv2.imread('photo2.jpeg')
cv2.imshow("Gray image",gray_image)
cv2.imshow("color image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Histogram of Grayscale Image
```python
import numpy as np
gray_image=cv2.imread('agray.jpg')
import matplotlib.pyplot as plt 
gray_hist=cv2.calcHist(gray_image,[0],None,[255],[0,255])
plt.figure(figsize=(10,6))
plt.subplot(1,2,1)
plt.imshow(gray_image)
plt.subplot(1,2,2)
plt.title("Histogram")
plt.xlabel("Grayscale value")
plt.ylabel("pixel count")
plt.stem(gray_hist)
plt.show()
```
### Histogram Equalization of Grayscale Image.
```python
import numpy as np
color_image=cv2.imread('vcolor.jpg')
color_img=cv2.cvtColor(color_image,cv2.COLOR_BGR2RGB)
import matplotlib.pyplot as plt 
color_hist=cv2.calcHist(color_img,[0],None,[255],[0,255])
plt.figure(figsize=(8,4))
plt.subplot(1,2,1)
plt.imshow(color_img)
plt.subplot(1,2,2)
plt.title("Histogram")
plt.xlabel("Colorscale value")
plt.ylabel("pixel count")
plt.stem(color_hist)
plt.show()
```

## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/user-attachments/assets/018aab6b-22b4-4ad7-970f-023ca4f921ab) 


### 
### Histogram of Grayscale Image
![Screenshot 2024-09-28 114102](https://github.com/user-attachments/assets/a3f7f15c-42bb-46cf-b22b-4721402e45f3)


### Histogram Equalization of Grayscale Image.
![Screenshot 2024-09-28 114514](https://github.com/user-attachments/assets/74fdf5ad-4da1-46aa-9d5e-57a9913f1766)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
