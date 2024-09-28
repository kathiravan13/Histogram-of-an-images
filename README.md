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
gray_image = cv2.imread('agray.jpg')
color_image = cv2.imread('vcolor.jpg')
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
![Screenshot 2024-09-28 105311](https://github.com/user-attachments/assets/b3fc969e-1931-4dce-9936-85715c7009ba)

### Histogram of Grayscale Image and 
![Screenshot 2024-09-28 105404](https://github.com/user-attachments/assets/0a04d475-64a3-4d40-b6ab-a58bbb5378ff)

### Histogram ofany channel of Color Image
![Screenshot 2024-09-28 105426](https://github.com/user-attachments/assets/fb3eec34-36f8-4aac-adbb-5815fb9fcdc2)

### Histogram Equalization of Grayscale Image.
![Screenshot 2024-09-28 105525](https://github.com/user-attachments/assets/39b67bf7-b6d8-489a-90a1-4bff2b56d2ce)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
