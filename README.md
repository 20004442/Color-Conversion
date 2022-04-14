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
color_image = cv2.imread('Heidi.jpg')
cv2.imshow('Original image',color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

# ii)Convert HSV to RGB and BGR

import cv2
color_image = cv2.imread('Heidi.jpg')
cv2.imshow('Original image', color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb

import cv2
color_image = cv2.imread('Heidi.jpg')
cv2.imshow('Original image',color_image)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

# iv)Split and Merge RGB Image

import cv2
image = cv2.imread('Heidi.jpg')
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
image = cv2.imread('Heidi.jpg')
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
![H2](https://user-images.githubusercontent.com/75235813/163431169-c07d04ad-82fa-4df1-94ad-548140f91a19.JPG)
![H1](https://user-images.githubusercontent.com/75235813/163431219-c43f34eb-ea19-45e4-900f-23f0171e6d06.JPG)



### ii) HSV to RGB and BGR
![H3](https://user-images.githubusercontent.com/75235813/163431260-6ac0db1b-abf0-4b34-9d7d-e81e8e47a8d6.JPG)
![H4](https://user-images.githubusercontent.com/75235813/163431283-7944729d-37ce-4f4a-bf55-b5d6cdf94260.JPG)


### iii) RGB and BGR to YCrCb
![H5](https://user-images.githubusercontent.com/75235813/163431314-f537016b-d689-48de-acf8-dcc26a673b03.JPG)
![H6](https://user-images.githubusercontent.com/75235813/163431327-69de2a62-3cfd-480d-8a15-c1164e421ba5.JPG)



### iv) Split and merge RGB Image
![H7](https://user-images.githubusercontent.com/75235813/163431365-d3299eb1-525d-4a5d-9860-3d8e252c07b1.JPG)
![H8](https://user-images.githubusercontent.com/75235813/163431393-7f7a7411-b5ad-4e32-8b12-5347b7a6b525.JPG)
![H9](https://user-images.githubusercontent.com/75235813/163431406-3db398cb-81f5-408f-a094-624ac17c41db.JPG)



### v) Split and merge HSV Image
![H11](https://user-images.githubusercontent.com/75235813/163431461-b57f044c-2a41-4330-bb8e-4a9a95f426da.JPG)
![H10](https://user-images.githubusercontent.com/75235813/163431481-f7dbdfe5-7a1e-4d5b-83ad-4873289c7375.JPG)
![H12](https://user-images.githubusercontent.com/75235813/163431507-0ee3c84a-87cc-4017-acc5-2da45c5d0a97.JPG)
![H13](https://user-images.githubusercontent.com/75235813/163431524-d25b99ba-2916-453f-96ba-d89edd7fc93b.JPG)




## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
