# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.

### Step3:
Display the histograms with their respective images.

### Step4:
Equalize the grayscale image.

### Step5:
Display the grayscale image.


## Program:
```python
# Developed By: ASHWIN A O 
# Register Number: 212220230005
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('PIC1.jpg')
plt.imshow(Gray_image)
plt.show()
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()


# Display the histogram of gray scale image and any one channel histogram from color image
Color_image=cv2.imread('PIC2.jpg')
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()



# Write the code to perform histogram equalization of the image. 
Gray_image=cv2.imread('LEO_GRAY.jpg',0)
equ=cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()






```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2022-04-27 003727](https://user-images.githubusercontent.com/75235601/165374848-6d0ecfc4-cd07-4317-a103-f97bbe79b537.jpg)


### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2022-04-27 003833](https://user-images.githubusercontent.com/75235601/165374901-2d3170dd-95ac-48c7-806c-d9c615a510bd.jpg)
![Screenshot 2022-04-27 003809](https://user-images.githubusercontent.com/75235601/165374908-3ef2b182-b529-488b-9f9f-789fc390f15e.jpg)



### Histogram Equalization of Grayscale Image

![Screenshot 2022-04-27 003930](https://user-images.githubusercontent.com/75235601/165374940-89b29596-f55e-4e2f-8be4-52e301fca58a.jpg)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
