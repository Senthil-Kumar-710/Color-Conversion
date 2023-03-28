# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 library and upload the image or capture an image.

### Step2:
Read the saved image using cv2.imread("filename.jpg").

### Step3:
Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) 
and similarly for other color formats. 

### Step4:
Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v]) 

### Step5:
Output the image using cv2.imshow("OUTPUT", image)


## Program:

### Developed By: Senthil Kumar S
### Register Number: 212221230091
# i) Convert BGR and RGB to HSV and GRAY
```python
import cv2
img = cv2.imread('goku.jpg')
cv2.imshow('original',img)

bgr2hsv = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR To HSV',bgr2hsv)

bgr2gray = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR To GRAY',bgr2gray)

rgb2hsv = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',rgb2hsv)

rgb2gray = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',rgb2gray)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

# ii)Convert HSV to RGB and BGR
```python
cv2.imshow('HSV',bgr2hsv)

hsv2rgb = cv2.cvtColor(bgr2hsv,cv2.COLOR_HSV2RGB)
cv2.imshow('HSVtoRGB',hsv2rgb)

hsv2bgr = cv2.cvtColor(bgr2hsv,cv2.COLOR_HSV2BGR)
cv2.imshow('HSVtoBGR',hsv2bgr)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

# iii)Convert RGB and BGR to YCrCb
```python
cv2.imshow('RGB',img)

rgb2YcrCb = cv2.cvtColor(img,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGBtoYCrCb',rgb2YcrCb)

bgr2YcrCb = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('BGRtoYCrCb',bgr2YcrCb)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

# iv)Split and Merge RGB Image
```python
b,g,r = cv2.split(img)
cv2.imshow("RED MODEL", r)
cv2.imshow("GREEN MODEL", g)
cv2.imshow("BLUE MODEL ", b)

merger = cv2.merge([b,g,r])
cv2.imshow("MERGED IMAGE", merger)

cv2.waitKey(0)
cv2.destroyAllWindows()
```



# v) Split and merge HSV Image
```python
cv2.imshow("INITIAL_HSV ", bgr2hsv)

h,s,v = cv2.split(bgr2hsv)
cv2.imshow("RED MODEL", h)
cv2.imshow("GREEN MODEL", s)
cv2.imshow("BLUE MODEL ", v)

merger = cv2.merge([h,s,v])
cv2.imshow("MERGED IMAGE", merger)

cv2.waitKey(0)
cv2.destroyAllWindows()
```



## Output:
### i) BGR and RGB to HSV and GRAY
![op1](https://user-images.githubusercontent.com/93860256/228265579-5ef49212-54f0-4229-a64a-6a69927778b2.png)

![op6](https://user-images.githubusercontent.com/93860256/228265765-fe814283-c550-4246-9a72-ddeeddb4d251.png)

![op20](https://user-images.githubusercontent.com/93860256/228275970-f0dc5744-1da9-483a-b4f0-8e51c58b15a8.PNG)
### ii) HSV to RGB and BGR
![op6](https://user-images.githubusercontent.com/93860256/228276202-e13fcec4-4f57-4d6b-931c-a35c842a9de8.png)

![op7](https://user-images.githubusercontent.com/93860256/228276364-a42b02aa-5e0c-4a8c-88b2-de59107fe136.png)

![op8](https://user-images.githubusercontent.com/93860256/228276549-3cb3a082-d640-49c9-8d3e-4689163e70d3.png)

### iii) RGB and BGR to YCrCb
![op10](https://user-images.githubusercontent.com/93860256/228276688-60cf5c76-5997-4822-b992-6fa9075d223e.png)

![op11](https://user-images.githubusercontent.com/93860256/228276792-56583c28-b7ef-41fe-b9ed-d1c794d65746.png)
### iv) Split and merge RGB Image
![op12](https://user-images.githubusercontent.com/93860256/228277015-1590c96e-7752-4b74-8d5b-ddf3ec3a3b39.png)

![op13](https://user-images.githubusercontent.com/93860256/228277007-f6677a7b-5432-4795-8dab-1b9f7db00ecf.png)

![op14](https://user-images.githubusercontent.com/93860256/228277022-5249f735-c9a3-460a-a998-fccd22f24f41.png)

![op15](https://user-images.githubusercontent.com/93860256/228277271-0092cf29-16fd-4c5b-b62e-e7297a496623.png)

### v) Split and merge HSV Image
![op16](https://user-images.githubusercontent.com/93860256/228277494-eb2abaa1-bd85-46ed-b349-ea395e8cdb63.png)

![op17](https://user-images.githubusercontent.com/93860256/228277482-e5f54ada-5319-476d-ad5d-ed5f31b37160.png)

![op18](https://user-images.githubusercontent.com/93860256/228277505-e963e65b-358b-49ee-b1e2-d5ee32996f2d.png)

![op19](https://user-images.githubusercontent.com/93860256/228277501-27575867-d4bb-4816-b743-730284e7164f.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
