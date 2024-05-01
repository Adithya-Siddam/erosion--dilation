## EX 09 Implementation-of-Erosion-and-Dilation
### Aim
To implement Erosion and Dilation using Python and OpenCV.
### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:<br>
Import the necessary pacakages

#### Step2:<br>
Create the text using cv2.putText

#### Step3:<br>
Create the structuring element

#### Step4:<br>
Erode the image


#### Step5: <br>
Dilate the Image

 
### Program:
```
NAME: S Adithya Chowdary.
REG.NO: 212221230100.
```

##### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
##### Create the Text using cv2.putText
``` Python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_TRIPLEX
cv2.putText(img ,'ADITHYA',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
##### Create the structuring element
``` Python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
##### Erode the image
``` Python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```
##### Dilate the image
``` Python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')



```
### Output:
#### Display the input Image
![image](https://github.com/Adithya-Siddam/erosion--dilation/assets/93427248/d3cfce44-081e-4c0c-b7be-816399270cfb)

#### Display the Eroded Image
![image](https://github.com/Adithya-Siddam/erosion--dilation/assets/93427248/676bac5a-6f45-4cf1-a6db-f4b0a8f11e68)

#### Display the Dilated Image
![image](https://github.com/Adithya-Siddam/erosion--dilation/assets/93427248/e79f65b7-52dc-4858-92b2-c0b972751fd1)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
