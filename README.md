# EX-6 EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.
### Step2:
Load a image using imread() from cv2 module.
### Step3:
Convert the image to grayscale
### Step4:
Using Sobel operator from cv2,detect the edges of the image.
### Step5:
Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## PROGRAM:
```
DEVELOPED BY: PRADEEP S
REGISTER NUMBER: 212222100034
```
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("lotus.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
**SOBEL X:**
  ```python
  sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y:**
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY:**
  ```python
  sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## ORIGINAL IMAGE:

![lotus](https://github.com/user-attachments/assets/2f87a940-a195-4565-88c7-4a03b30992e1)

### SOBEL EDGE DETECTOR:

![lot1](https://github.com/user-attachments/assets/db3defc2-6d51-4630-abdb-14cd2bf99408)

![lot2](https://github.com/user-attachments/assets/56d70f3a-618c-446d-856f-7ce51e8e1975)

![lot3](https://github.com/user-attachments/assets/7e97ba23-12bf-4b3e-8cb6-49acb9315ff4)

### LAPLACIAN EDGE DETECTOR

![lot4](https://github.com/user-attachments/assets/1312a215-bfed-42a1-a90b-40d58ee4bc50)


### CANNY EDGE DETECTOR

![lot5](https://github.com/user-attachments/assets/f37f967f-767b-444c-99ca-4bde75f6100c)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
