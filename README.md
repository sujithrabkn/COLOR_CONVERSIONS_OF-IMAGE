# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
1.  Draw a line from the top-left to the bottom-right of the image.

2.	Draw a circle at the center of the image.

3.	Draw a rectangle around a specific region of interest in the image.

4.	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
1.	Convert the image from RGB to HSV and display it.
2.	Convert the image from RGB to GRAY and display it.
3.	Convert the image from RGB to YCrCb and display it.
4.	Convert the HSV image back to RGB and display it.

### Step4:
1.	Access and print the value of the pixel at coordinates (100, 100).
2.	Modify the color of the pixel at (200, 200) to white.

### Step5:
Resize the original image to half its size and display it.
### Step6:
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
1.	Flip the original image horizontally and display it.
2.	Flip the original image vertically and display it.

### Step8:
Save the final modified image to your local directory.
   

### Developed By: SUJITHRA B K N
### Register Number: 212222230153


## Program & Output:

### i)Read and Display an Image
Load an image from your local directory and display it.
```
import cv2 
image=cv2.imread('f.png',1)
image =cv2.resize(image, (400, 300))
cv2.imshow('WINDOW',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-09 140603](https://github.com/user-attachments/assets/8e2c2ec1-6f92-4d56-9e03-f77c7babfd9f)



### ii)Draw Shapes and Add Text
(1) Draw a line from the top-left to the bottom-right of the image.
```
import cv2
image = cv2.imread("f.png")
image = cv2.resize(image, (400, 300))
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (255,0,0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 140625](https://github.com/user-attachments/assets/e17d698d-4b12-4734-ba4e-2da2f1b85f5c)




(2) Draw a circle at the center of the image.
```
import cv2
image = cv2.imread("f.png")
image = cv2.resize(image, (400, 300))
height, width, _ = image.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(image, center_coordinates, 120, (0, 255, 0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-09 140640](https://github.com/user-attachments/assets/091b9155-2bc7-4632-9be0-9d30aff022ed)


(3) Draw a rectangle around a specific region of interest in the image.
```
import cv2
image = cv2.imread("f.png")
image = cv2.resize(image, (400, 300))
start = (150, 100)
stop = (300, 200)
color = (255, 255, 100)
thickness = 10           
res_img = cv2.rectangle(image, start, stop, color, thickness)
cv2.imshow('WINDOW', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-09 141008](https://github.com/user-attachments/assets/49e51559-40d8-46cf-bc9f-3b0bd420c25f)


(4) Add the text "OpenCV Drawing" at the top-left corner of the image.
```
import cv2
image = cv2.imread("f.png")
image = cv2.resize(image, (400, 300))
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-09 141044](https://github.com/user-attachments/assets/f295f325-3e09-4ddc-8fec-614217b2338c)


### iii)Image Color Conversion

(1) Convert the image from RGB to HSV and display it
```
import cv2
image = cv2.imread('f.png',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 141122](https://github.com/user-attachments/assets/dfa6a444-c37d-402d-91f5-5f4684addf22)
![Screenshot 2024-09-09 141116](https://github.com/user-attachments/assets/79512306-b4fd-480f-902c-23844d4a883a)



(2) Convert the image from RGB to GRAY and display it.
```
import cv2
image = cv2.imread('f.png',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 141122](https://github.com/user-attachments/assets/dfa6a444-c37d-402d-91f5-5f4684addf22)
![Screenshot 2024-09-09 141206](https://github.com/user-attachments/assets/1a99ef6f-abce-408c-a4ce-b224c83d8613)


(3) Convert the image from RGB to YCrCb and display it.
```
import cv2
image = cv2.imread('f.png',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 141122](https://github.com/user-attachments/assets/dfa6a444-c37d-402d-91f5-5f4684addf22)
![Screenshot 2024-09-09 141242](https://github.com/user-attachments/assets/cd1fe6a9-e3f7-4fe9-8784-6de96635a498)


(4) Convert the HSV image back to RGB and display it.
```
import cv2
image = cv2.imread('f.png',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 141122](https://github.com/user-attachments/assets/dfa6a444-c37d-402d-91f5-5f4684addf22)
![Screenshot 2024-09-09 141340](https://github.com/user-attachments/assets/c8563dcc-761e-48e6-8b80-8953a3a18ad8)


### iv)Access and Manipulate Image Pixels

(1) Access and print the value of the pixel at coordinates (100, 100)
```
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
![Screenshot 2024-09-09 142011](https://github.com/user-attachments/assets/087a9188-5a6a-4b50-93c1-9a058262f83c)


(2) Modify the color of the pixel at (200, 200) to white
```
import cv2
image = cv2.imread('f.png',1)
image = cv2.resize(image,(400,300))
cv2.imshow('ORIGINAL IMAGE',image)
image[200, 200] = [255, 255, 255] 
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 141519](https://github.com/user-attachments/assets/1ec49499-e63f-43b2-9193-2f8215d56edc)

![Screenshot 2024-09-09 141504](https://github.com/user-attachments/assets/56679372-51da-4f5d-aba7-057d5fa6eb9a)


### v)Image Resizing
Resize the original image to half its size and display it.
```
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-09 141122](https://github.com/user-attachments/assets/dfa6a444-c37d-402d-91f5-5f4684addf22)
![Screenshot 2024-09-09 141550](https://github.com/user-attachments/assets/fa9712ed-c600-4a0b-8da2-5be98e11c8ea)



### vi)Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
import cv2
image = cv2.imread('f.png',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 141630](https://github.com/user-attachments/assets/f7b7078c-97d8-46b2-b466-38d315e6df65)



### vii)Image Flipping
(1) Flip the original image horizontally and display it.
```
import cv2
image = cv2.imread("f.png")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_180)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-09 141122](https://github.com/user-attachments/assets/dfa6a444-c37d-402d-91f5-5f4684addf22)
![Screenshot 2024-09-09 141703](https://github.com/user-attachments/assets/994b3925-39c2-4a6f-8ad0-b239a9dd0e05)


(2) Flip the original image vertically and display it.
```
import cv2
image = cv2.imread("f.png")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 141122](https://github.com/user-attachments/assets/dfa6a444-c37d-402d-91f5-5f4684addf22)
![Screenshot 2024-09-09 141759](https://github.com/user-attachments/assets/0b876746-51f5-443e-b02a-882f52918b26)



### viii)Write and Save the Modified Image
Save the final modified image to your local directory.
```
import cv2
img = cv2.imread("f.png")
img = cv2.resize(img,(300,200))
cv2.imwrite('boat_pic.jpg',img)
```

![Screenshot 2024-09-09 142020](https://github.com/user-attachments/assets/80cc4672-5bb4-449a-b297-133795cbf111)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







