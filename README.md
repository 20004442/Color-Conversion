# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 and save and image as filename.jpg

### Step2:
Use imread(filename, flags) to read the file.

### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:
Split and merge the image using cv2.split and cv2.merge commands

### Step5:
End the program and close the output image windows.

## Program:
```python
# Developed By: B.Kavya
# Register Number: 212220230007
# i) Convert BGR and RGB to HSV and GRAY

import cv2
color_image = cv2.imread('bts.jpg')
cv2.imshow('Original image',color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

# ii)Convert HSV to RGB and BGR

import cv2
color_image = cv2.imread('bts.jpg')
cv2.imshow('Original image', color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb

import cv2
color_image = cv2.imread('bts.jpg')
cv2.imshow('Original image',color_image)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

# iv)Split and Merge RGB Image

import cv2
image = cv2.imread('bts.jpg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
Merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',Merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()

# v) Split and merge HSV Image

import cv2
image = cv2.imread('bts.jpg')
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue-Image',h)
cv2.imshow('Saturation-Image',s)
cv2.imshow('Gray-Image',v)
Merged_HSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()

```
## Output:
### i) BGR and RGB to HSV and GRAY
![DIP31](https://user-images.githubusercontent.com/75235813/163426897-47371b84-de53-473c-b014-653ec08732b2.JPG)
![DIP32](https://user-images.githubusercontent.com/75235813/163426920-2499a8e9-a102-48fd-8243-51f873cd2ee4.JPG)


### ii) HSV to RGB and BGR
![DIP33](https://user-images.githubusercontent.com/75235813/163426979-00ef3a59-5639-4202-bcd6-847d4e8b35c5.JPG)
![DIP34](https://user-images.githubusercontent.com/75235813/163427005-d3df5e1d-7336-4a4a-8347-627e8d319886.JPG)

### iii) RGB and BGR to YCrCb
![DIP35](https://user-images.githubusercontent.com/75235813/163427093-5c0ec8b1-4433-4361-b2ab-2e534b95fffa.JPG)
![DIP36](https://user-images.githubusercontent.com/75235813/163427117-1d3a205a-0e7a-486b-80cb-75bfe004e016.JPG)


### iv) Split and merge RGB Image
![DIP37](https://user-images.githubusercontent.com/75235813/163427144-85bfbcbd-5d85-4415-8314-2f2790296044.JPG)
![DIP38](https://user-images.githubusercontent.com/75235813/163427171-23a3f8a9-dd0e-4d5e-9277-d6fa4d5ee8b7.JPG)
![DIP39](https://user-images.githubusercontent.com/75235813/163427188-e101ff4e-f892-4ee1-a9ee-9be3ffc9aee0.JPG)


### v) Split and merge HSV Image
![DIP40](https://user-images.githubusercontent.com/75235813/163427228-5a2b8d4e-7994-4a1f-a7c4-d602921867af.JPG)
![DIP41](https://user-images.githubusercontent.com/75235813/163427256-8e6e8d4c-3510-46f6-ab3f-9197c642d067.JPG)
![DIP43](https://user-images.githubusercontent.com/75235813/163427304-3bf514b0-8c75-4ff5-aaed-2eca325b5b3e.JPG)
![DIP44](https://user-images.githubusercontent.com/75235813/163427345-d9027e39-ed9d-44e2-99dd-844726373809.JPG)



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
