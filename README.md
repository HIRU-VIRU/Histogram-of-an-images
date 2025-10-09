# Histogram-of-an-images
# Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

# Software Required:
Anaconda - Python 3.7

# Algorithm:
## Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().

## Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

## Step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

## Step5:
The Histogram of gray scale image and color image is shown.


# Program:

## Developed By:HIRUTHIK SUDHAKAR
## Register Number: 212223240054

```python
import cv2
import matplotlib.pyplot as plt 
Gray_image=cv2.imread("/content/eagle.jpg")
plt.imshow(Gray_image)
plt.show()
Color_image=cv2.imread("/content/heidi.jpg")
plt.imshow(Color_image)
plt.show()
### code to find the histogram of gray scale image and color image channels.

hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('gray_scale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

# Display the histogram of gray scale image and any one channel histogram from color image

hist1 = cv2.calcHist([Color_image],[0],None,[256],[0,256]) 
plt.figure()
plt.title("Histogram")
plt.xlabel('color_scale value') 
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

# Write the code to perform histogram equalization of the image.

equ1=cv2.equalizeHist(cv2.imread('/content/heidi.jpg',0)) 
equ=cv2.cvtColor(equ1,cv2.COLOR_BGR2RGB) 
plt.title("Equalised Image")
plt.axis("off")
plt.imshow(equ) 
plt.show()

# Histogram for the equalized image
hist_eq = cv2.calcHist([equ1], [0], None, [256], [0, 256])
plt.figure()
plt.title("Histogram of Equalized Image")
plt.xlabel('Gray Scale Value')
plt.ylabel('Pixel Count')
plt.stem(hist_eq)
plt.show()

```

# Output:
## Input Grayscale Image and Color Image
<img width="552" height="261" alt="image" src="https://github.com/user-attachments/assets/b66f9d6f-5e34-4948-98cb-31a9da3aa555" />
<img width="543" height="418" alt="image" src="https://github.com/user-attachments/assets/05919132-7d08-4016-9fbf-f75e6c024fc5" />



## Histogram of Grayscale Image and any channel of Color Image

<img width="589" height="455" alt="image" src="https://github.com/user-attachments/assets/8683ac87-22d6-4f33-a0a0-462400d4380a" />

## Histogram Equalization of Grayscale Image.

<img width="589" height="455" alt="image" src="https://github.com/user-attachments/assets/de5a40c9-4f5a-4440-b155-51580b8d12d7" />

<img width="507" height="411" alt="image" src="https://github.com/user-attachments/assets/7369cd05-106e-49d8-a16e-71b5fc6abb8d" />


<img width="580" height="455" alt="download" src="https://github.com/user-attachments/assets/b177b0f0-5948-4e5c-8b12-19456b30f139" />

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
