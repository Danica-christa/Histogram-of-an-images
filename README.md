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
```python
# Developed By: DANICA CHRISTA
# Register Number: 212223240022

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('img0.jpg')
color_image = cv2.imread('img1.jpg')
cv2.imshow("Gray image",gray_image)
cv2.imshow("color image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()      


import numpy as np
gray_image=cv2.imread('img0.jpg')
import matplotlib.pyplot as plt 
gray_hist=cv2.calcHist(gray_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale value")
plt.ylabel("pixel count")
plt.stem(gray_hist)
plt.show()


import numpy as np
color_image=cv2.imread('img1.jpg')
import matplotlib.pyplot as plt 
color_hist=cv2.calcHist(color_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(color_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Colorscale value")
plt.ylabel("pixel count")
plt.stem(color_hist)
plt.show()


import cv2
gray_image = cv2.imread("img0.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()







```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2025-04-26 122938](https://github.com/user-attachments/assets/b1142b01-ff7f-4e97-afb9-ebf6e95dc072)

![Screenshot 2025-04-26 123021](https://github.com/user-attachments/assets/1f74d423-fb37-46e7-b335-6005973969ff)

![Screenshot 2025-04-26 123653](https://github.com/user-attachments/assets/3fe4acfd-1c21-42be-8025-c7b3f4443777)

![Screenshot 2025-04-26 123659](https://github.com/user-attachments/assets/114eee8e-d109-4bcb-aa01-924dd1ff2fa0)



### Histogram of Grayscale Image and any channel of Color Image
 ![Screenshot 2025-04-26 123638](https://github.com/user-attachments/assets/00241f92-78b6-4077-81cd-3fae8c95205b)

![Screenshot 2025-04-26 123647](https://github.com/user-attachments/assets/8adc83bd-407d-42ae-958a-0a07527caa60)




### Histogram Equalization of Grayscale Image.
![image](https://github.com/user-attachments/assets/4618cee1-8dcc-4d47-909d-cd4a3078f815)





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
