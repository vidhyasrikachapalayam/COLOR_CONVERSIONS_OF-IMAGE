# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

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
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


##### Program:
### Developed By:Vidhyasri k
### Register Number: 212222230170


## Output:

### i)Read and Display an Image
```
import cv2
image=cv2.imread('panda.jpg',1)
cv2.imshow('Image Window', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/bab11065-44ad-481c-827e-6be855b52567)

### ii)Draw Shapes and Add Text
i)Draw a line from the top-left to the bottom-right of the image
```
import cv2
img = cv2.imread("panda.jpg")
res = cv2.line(img, (0, 0), (1099, 799), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
![image](https://github.com/user-attachments/assets/19e3d705-59db-4cf2-8198-fcad4fc43566)

ii)Draw a circle at the center of the image.
```
import cv2

# Load the image
img = cv2.imread("panda.jpg")

# Get the dimensions of the image
height, width, _ = img.shape

# Calculate the center of the image
center_coordinates = (width // 2, height // 2)

# Draw a circle at the center of the image
res = cv2.circle(img, center_coordinates, 150, (255, 0, 0), 10)

# Display the image with the circle
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/5cb60bb0-cd7b-43dc-a5a3-ceb35f8b1264)

iii)Draw a rectangle around a specific region of interest in the image.
```
import cv2

img = cv2.imread("panda.jpg")
start=(0,0)
stop=(318,200)
color=(100,255,100)
thickness=10
res_img=cv2.rectangle(img,start,stop,color,thickness)
# Display the HSV image
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/00436f97-f39d-47da-8327-0b2bae8f6d2b)

iv)Add the text "PANDA" at the top-left corner of the image.
```
import cv2

# Load the image
img = cv2.imread("panda.JPG")

# Define the text to be added and its position
text = "OPENCV DRAWING"
position = (50, 50)  # Positioning the text at the top-left corner

# Set the font, scale, color, and thickness of the text
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255)  # White color
thickness = 2

# Add the text to the image
res = cv2.putText(img, text, position, font, font_scale, color, thickness, cv2.LINE_AA)

# Display the image with the text
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/c7352658-b222-4c45-a3c5-1a1289cb5fe6)

### iii)Image Color Conversion
i)Convert the image from RGB to HSV and display it.
```
import cv2
img = cv2.imread('panda.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/b70a067b-8f78-468c-a30e-3aa48f509a0b)

ii.)Convert the image from RGB to GRAY and display it.
```
import cv2
img = cv2.imread('panda.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/d53cbd8f-0b8b-4de4-906f-17f740e1250c)

iii.)Convert the image from RGB to YCrCb and display it.
```
import cv2
img = cv2.imread('panda.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![image](https://github.com/user-attachments/assets/120abf91-2adf-48d3-b603-a4ca2819f151)

iv.)Convert the HSV image back to RGB and display it.
```
import cv2
img = cv2.imread('panda.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![image](https://github.com/user-attachments/assets/cce63c63-54fe-4352-b602-cfba404f1945)


### iv)Access and Manipulate Image Pixels
```
import cv2

# Load and resize the image
img = cv2.imread('panda.jpg', 1)
img = cv2.resize(img, (300, 200))

# Show the original image
cv2.imshow('Original Image', img)

# 1. Access and print the value of the pixel at coordinates (100, 100)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")

# 2. Modify the color of the pixel at (199, 199) to white
img[199, 199] = [255, 255, 255]  # Setting the pixel value to white (BGR)

# Display the modified image
cv2.imshow('Modified Image', img)

# Wait for a key press and close the windows
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/97fd2db4-a2e9-40b7-b99e-01ff88b059e4)



### v)Image Resizing
```
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(image, (300, 400))
cv2.imshow('Original',image)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/4b7910d9-aca4-4d27-8853-03537b7d7053)


### vi)Image Cropping
```
import cv2

# Load the image
image1=cv2.imread('panda.jpg',1)

# Define the starting point and size of the ROI
x, y = 50, 50
width, height = 100, 100

# Crop the ROI
roi = image1[y:y + height, x:x + width]

# Display the cropped ROI
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/8e7f0a7d-0423-4bdd-8d99-3e8b58a1b0da)


### vii)Image Flipping
i.)Flip the original image horizontally and display it.
```
import cv2
img = cv2.imread("panda.jpg")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/5901c7e5-253b-42b3-81b2-971864480a71)


ii.)Flip the original image vertically and display it
```
import cv2

img = cv2.imread("panda.JPG")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
# Display the HSV image
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/7fdbc046-0452-4136-8e4f-77f85a07570d)


### viii)Write and Save the Modified Image
```
 cv2.imwrite('panda.jpg',image)
```
![image](https://github.com/user-attachments/assets/b3225744-8e45-4c1b-9ef8-5ad560ef5430)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







