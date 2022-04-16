# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Read an image using imread() and Convert BGR and RGB to HSV and GRAY
using:
```
cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
```

### Step2:
Convert HSV to RGB and BGR
using:
```
cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
```

### Step3:
Convert RGB and BGR to YCrCb
using:
```
cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
```

### Step4:
Split and Merge RGB Image
using:
```
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.merge((blue,green,red))
```

### Step5:
Split and merge HSV Image
using:
```
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)
cv2.merge((h,s,v))
```

## Program:

# Developed By: S. Sanjna Priya
# Register Number:212220230043
# i) Convert BGR and RGB to HSV and GRAY
```
import cv2
image=cv2.imread("simp.jpg")
cv2.imshow("212220230043",image)
BGR_HSV=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("BGR to HSV image",BGR_HSV)
BGR_GRAY=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("BGR to GRAY image",BGR_GRAY)
RGB_HSV=cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow("RGB to HSV image",RGB_HSV)
RGB_GRAY=cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow("RGB to GRAY image",RGB_GRAY)
cv2.imshow("picz",image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

# ii)Convert HSV to RGB and BGR
```
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("HSV image",hsv)
HSV_RGB=cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.imshow("HSV to RGB image",HSV_RGB)
HSV_BGR=cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow("HSV to BGR image",HSV_BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

# iii)Convert RGB and BGR to YCrCb
```
RGB_YCrCb=cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.imshow("RGB to YCrCb image",RGB_YCrCb)
BGR_YCrCb=cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR to YCrCb image",BGR_YCrCb)
cv2.imshow("picz",image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

# iv)Split and Merge RGB Image
```
blue = image[:,:,0]
cv2.imshow("Blue Split",blue)
green = image[:,:,1]
cv2.imshow("Green Split",green)
red = image[:,:,2]
cv2.imshow("Red Split",red)
merged=cv2.merge((blue,green,red))
cv2.imshow("Merged Image",merged)
cv2.imshow("new pic",image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

# v) Split and merge HSV Image
```
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)
cv2.imshow('h_plane', h)
cv2.imshow('s_plane', s)
cv2.imshow('v_plane', v)
mergedhsv=cv2.merge((h,s,v))
cv2.imshow("HSV image",hsv)
cv2.imshow('Merged HSV',mergedhsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### i) BGR and RGB to HSV and GRAY
![EXPT3 IMG1](https://user-images.githubusercontent.com/75234965/163677013-992dc3ba-724d-4511-8871-08f803d643be.PNG)

![EXPT3 IMG2](https://user-images.githubusercontent.com/75234965/163677022-1a0bc32a-707a-49ea-8cf6-d1e9df962876.PNG)

### ii) HSV to RGB and BGR
![EXPT3 IMG3](https://user-images.githubusercontent.com/75234965/163677032-503ea3f2-fb66-4d8e-a52e-e6d5eba2dda8.PNG)

### iii) RGB and BGR to YCrCb
![EXPT3 IMG4](https://user-images.githubusercontent.com/75234965/163677040-51cbaa0d-a794-468e-9ea8-82c6e02cdb9a.PNG)

### iv) Split and merge RGB Image
![EXPT3 IMG5](https://user-images.githubusercontent.com/75234965/163677048-c1bed602-28b1-4510-966c-9ce835c812ba.PNG)

![EXPT3 IMG6](https://user-images.githubusercontent.com/75234965/163677051-b0402cf1-06b5-488a-96c8-92e02727a2c4.PNG)

### v) Split and merge HSV Image
![EXPT3 IMG7](https://user-images.githubusercontent.com/75234965/163677060-df50bfd1-da3d-40d6-bd05-5ab755e7cc39.PNG)

![EXPT3 IMG8](https://user-images.githubusercontent.com/75234965/163677065-4394eeb0-ab10-41e2-8fa1-754cdc689de8.PNG)

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
