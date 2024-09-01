# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By: SUJITHRA B K N 
### Register Number: 212222230153


<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
import cv2
image=cv2.imread('photogragh.jpg',1)
image = cv2.resize(image, (400, 300))
cv2.imshow('suji',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:

![Screenshot 2024-09-01 073438](https://github.com/user-attachments/assets/b0216b77-947b-476d-9921-4dcf572ac291)



 
  </td>
  </tr>

   <tr>
    <td width=50%>

### ii) Write the image
```Python
    cv2.imwrite('b.jpg',image)
```
  </td>
  <td>

### OUTPUT:

![Screenshot 2024-09-01 075343](https://github.com/user-attachments/assets/ad03191b-e46b-4d66-953b-45e4aed4c2ad)

  </td>
  </tr>
  <tr>
    <td width=50%>

### iii) Shape of the Image
```Python
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:

![Screenshot 2024-09-01 075325](https://github.com/user-attachments/assets/a0bb6a86-466d-4f22-98dc-1ccafd156a6f)


  </td>
  </tr>
  <tr>
    <td>
      
### iv) Access rows and columns
```Python
    import random
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                     random.randint(0,255),
                     random.randint(0,255)] 
cv2.imshow('suji-1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

### OUTPUT:

![Screenshot 2024-09-01 073651](https://github.com/user-attachments/assets/ec1c7f1d-a487-469b-b2e7-600f5b927533)

  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v) Cut and paste portion of image

 ```Python
    image=cv2.imread('photogragh.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[130:200,110:190]
image[110:180,120:200] = tag
cv2.imshow('suji-2',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
  </td>
  <td>

### OUTPUT:

![Screenshot 2024-09-01 073731](https://github.com/user-attachments/assets/79c03d05-8b5c-4afc-81ef-ce7b956e0538)

  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY

```python
img = cv2.imread('photogragh.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![Screenshot 2024-09-01 073839](https://github.com/user-attachments/assets/dde91f9f-7ee6-4736-85a6-70e98b2db265)

![Screenshot 2024-09-01 073910](https://github.com/user-attachments/assets/e1206cf8-06cc-49d4-a23b-88c321dd2f1d)

![Screenshot 2024-09-01 073903](https://github.com/user-attachments/assets/198407be-af25-428e-87c1-4961c23b4044)

![Screenshot 2024-09-01 073855](https://github.com/user-attachments/assets/da378758-d4b7-4687-b92d-0bf7d00587fc)

![Screenshot 2024-09-01 073845](https://github.com/user-attachments/assets/4b8898f8-f02e-4178-93b6-bf2382450531)


### vii) HSV to RGB and BGR
```python
img = cv2.imread('photogragh.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![Screenshot 2024-09-01 073959](https://github.com/user-attachments/assets/c472db1f-8f43-49cd-a281-bd283cdac4a1)

![Screenshot 2024-09-01 074018](https://github.com/user-attachments/assets/36b4051b-518a-4488-95a6-15d6df6a6ecb)

![Screenshot 2024-09-01 074011](https://github.com/user-attachments/assets/a1c0cd63-34f7-45bb-a100-1330fbc3fe9e)

### viii) RGB and BGR to YCrCb
```python
img = cv2.imread('photogragh.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![Screenshot 2024-09-01 074107](https://github.com/user-attachments/assets/61922be0-dde2-43bb-a2d0-35d9bfff782f)

![Screenshot 2024-09-01 074115](https://github.com/user-attachments/assets/f2ded9b0-3665-42d9-a3c5-eb7931e1447c)

![Screenshot 2024-09-01 074123](https://github.com/user-attachments/assets/098cf311-cf06-4027-b4ad-8d87e3a551b5)


### ix) Split and merge RGB Image
```python
img = cv2.imread('photogragh.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![Screenshot 2024-09-01 074219](https://github.com/user-attachments/assets/aacbb552-fde8-4f8d-bc1b-90c53fc2ef52)


### x) Split and merge HSV Image
```python
img = cv2.imread("photogragh.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![Screenshot 2024-09-01 074317](https://github.com/user-attachments/assets/aea49200-d9bf-49d8-a244-91162f59db7b)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
