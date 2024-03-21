# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: MANOGARAN S
# Register Number: 212223240081
import cv2
import matplotlib.pyplot as plt

# Histogram for Gray scale and Color image
 
gray_image = cv2.imread('greyscale.jpg')
color_image = cv2.imread('colour.jpeg')
plt.imshow(gray_image)
plt.show()
plt.imshow(color_image)
plt.show()
hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('GrayScaleValue')
plt.ylabel('PixelCount')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity Value')
plt.ylabel('PixelCount')
plt.stem(hist1)
plt.show()



# Equalized Image
import cv2
Gray_image=cv2.imread('greyscale.jpg',0)
equ = cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-03-21 223037](https://github.com/manogarans/Histogram-of-an-images/assets/139331782/ab1ffc03-038c-4ee9-9c57-79d8abe71d36)


### Histogram of Grayscale Image and any channel of Color Image

![Screenshot 2024-03-21 223058](https://github.com/manogarans/Histogram-of-an-images/assets/139331782/33503d33-e764-47b0-9999-4f81418b9437)


### Histogram Equalization of Grayscale Image.
## Original:
![Screenshot 2024-03-21 223633](https://github.com/manogarans/Histogram-of-an-images/assets/139331782/16ca83b9-07c6-4629-96fd-d53759901844)
## grayscale image:
![Screenshot 2024-03-21 223627](https://github.com/manogarans/Histogram-of-an-images/assets/139331782/8a885f7d-7958-47ea-a3bd-d035d5428136)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
