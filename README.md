# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:

### Step1:
Import cv2 library and upload the image or capture an image.
</br>
### Step2:
Read the saved image using cv2.imread("filename.jpg").
</br>
### Step3:
Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) and similarly for other color formats.
</br>
###  Step4:
Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v])
</br>
### Step5:
Output the image using cv2.imshow("OUTPUT", image)
</br>

## Program:
```python
# Developed By: Revathi Dayalan
# Register Number: 212221240045

# i) Convert BGR and RGB to HSV and GRAY
import cv2
bfly_color_image = cv2.imread('butterfly.jpg')
cv2.imshow('original image',bfly_color_image)
hsv_image = cv2.cvtColor(bfly_color_image,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_image)
hsv_image1 = cv2.cvtColor(bfly_color_image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv_image1)
gray_image = cv2.cvtColor(bfly_color_image,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray_image)
gray_image1 = cv2.cvtColor(bfly_color_image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()



# ii)Convert HSV to RGB and BGR
import cv2
img = cv2.imread("butterfly.jpg")
img1= cv2.resize(img, (270,190))
hsv = cv2.cvtColor(img1 , cv2.COLOR_BGR2HSV)
cv2.imshow("INITIAL_HSV ", hsv)
hsv_rgb = cv2.cvtColor(hsv, cv2.COLOR_HSV2RGB)
cv2.imshow("HSV2RGB", hsv_rgb)
hsv_bgr = cv2.cvtColor(hsv, cv2.COLOR_HSV2BGR)
cv2.imshow("HSV2BGR", hsv_bgr)
cv2.waitKey(0)
cv2.destroyAllWindows()


# iii)Convert RGB and BGR to YCrCb
import cv2
img = cv2.imread("butterfly.jpg")
img1= cv2.resize(img, (270,190))
cv2.imshow("BGR_COLOR ", img1)
img_ycrcb = cv2.cvtColor(img1 , cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR_YCRCB ", img_ycrcb)
img_bgr = cv2.cvtColor(img1, cv2.COLOR_BGR2RGB)
cv2.imshow("RGB COLOR", img_bgr)
img_bgr_y = cv2.cvtColor(img_bgr, cv2.COLOR_BGR2YCrCb)
cv2.imshow("RGB2YCrCb", img_bgr_y)
cv2.waitKey(0)
cv2.destroyAllWindows()


# iv)Split and Merge RGB Image
import cv2
img = cv2.imread("butterfly.jpg")
img1= cv2.resize(img, (270,190))
cv2
b,g,r = cv2.split(img1)
cv2.imshow("RED MODEL", r)
cv2.imshow("GREEN MODEL", g)
cv2.imshow("BLUE MODEL ", b)
merger = cv2.merge([b,g,r])
cv2.imshow("MERGED IMAGE", merger )
cv2.waitKey(0)
cv2.destroyAllWindows()


# v) Split and merge HSV Image
import cv2
img = cv2.imread("butterfly.jpg")
img1= cv2.resize(img, (270,190))
hsv = cv2.cvtColor(img1 , cv2.COLOR_BGR2HSV)
cv2.imshow("INITIAL_HSV ", hsv)
h,s,v = cv2.split(hsv)
cv2.imshow("RED MODEL", h)
cv2.imshow("GREEN MODEL", s)
cv2.imshow("BLUE MODEL ", v)
merger = cv2.merge([h,s,v])
cv2.imshow("MERGED IMAGE", merger )
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### i) BGR and RGB to HSV and GRAY
![o1](https://user-images.githubusercontent.com/96000574/166145119-e6adaad4-0d02-45a0-8ed5-62822cddf48f.PNG)


<br>
<br>

### ii) HSV to RGB and BGR

![o2](https://user-images.githubusercontent.com/96000574/166145126-b653b805-6936-4c89-a8de-8ab7b612281c.PNG)

<br>
<br>

### iii) RGB and BGR to YCrCb
![o3](https://user-images.githubusercontent.com/96000574/166145132-e08374f5-c974-473c-8dc5-d3f55733fc8c.PNG)


<br>
<br>

### iv) Split and merge RGB Image
![o4](https://user-images.githubusercontent.com/96000574/166145134-dc4e93a7-f09d-449d-9e65-7ed5c0981da3.PNG)


<br>
<br>

### v) Split and merge HSV Image

![o5](https://user-images.githubusercontent.com/96000574/166145138-6992537f-baa2-4f09-ad9d-48cc9f403603.PNG)

<br>
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
