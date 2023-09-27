# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Load the image using a suitable library like OpenCV.

### Step2:
Convert the image to grayscale using cvtColor() if needed.

### Step3:
Calculate the histogram using calcHist() and plot it with Matplotlib.

### Step4:
Perform histogram equalization using equalizeHist() for enhanced contrast.

### Step5:
Visualize results by plotting histograms and displaying original and equalized images side by side.


## Program:
```
Developed By: Mourise jane
Register Number: 212222230085
```


# Write your code to find the histogram of gray scale image and color image channels.

```
For a grayscale image
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load a grayscale image
image_path = 'G.jpg'
gray_image = cv2.imread(image_path, cv2.IMREAD_GRAYSCALE)

# Calculate histogram
hist = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

# Plot the histogram
plt.plot(hist)
plt.xlabel('Pixel Value')
plt.ylabel('Frequency')
plt.title('Histogram of Grayscale Image')
plt.show()
```
```
For colour image

import cv2
import numpy as np
import matplotlib.pyplot as plt

#### Load a color image
image_path = 'M.jpg'
color_image = cv2.imread(image_path, cv2.IMREAD_COLOR)

#### Convert color image to grayscale
gray_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2GRAY)

#### Calculate histogram
hist = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

#### Plot the histogram
plt.plot(hist)
plt.xlabel('Pixel Value')
plt.ylabel('Frequency')
plt.title('Histogram of color Image')
plt.show()
```



# Display the histogram of gray scale image and any one channel histogram from color image
```
Histogram of Grayscale image

import cv2
import numpy as np
import matplotlib.pyplot as plt

#### Load a grayscale image
image_path = 'G.jpg'
gray_image = cv2.imread(image_path, cv2.IMREAD_GRAYSCALE)

#### Calculate histogram
hist = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

#### Plot the histogram
plt.plot(hist)
plt.xlabel('Pixel Value')
plt.ylabel('Frequency')
plt.title('Histogram of Grayscale Image')
plt.show()

```


# Write the code to perform histogram equalization of the image. 

```

import cv2
import numpy as np
import matplotlib.pyplot as plt

#### Load a grayscale image
image_path = 'G.jpg'
gray_image = cv2.imread(image_path, cv2.IMREAD_GRAYSCALE)

#### Perform histogram equalization
equalized_image = cv2.equalizeHist(gray_image)

#### Calculate histograms before and after equalization
hist_before = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
hist_after = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])

#### Plot the histograms
plt.figure(figsize=(10, 6))

plt.subplot(2, 1, 1)
plt.plot(hist_before)
plt.title('Original Histogram')
plt.xlabel('Pixel Value')
plt.ylabel('Frequency')

plt.subplot(2, 1, 2)
plt.plot(hist_after)
plt.title('Equalized Histogram')
plt.xlabel('Pixel Value')
plt.ylabel('Frequency')

plt.tight_layout()
plt.show()

#### Display the original and equalized images
cv2.imshow('Original Grayscale Image', gray_image)
cv2.imshow('Equalized Grayscale Image', equalized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()







```
## Output:
### Input Grayscale Image and Color Image


![G](https://github.com/Jayakrishnan22003251/HISTOGRAM/assets/120232371/9edb50f5-1c8d-478a-be0e-7e0d9b20f49c)

![M](https://github.com/Jayakrishnan22003251/HISTOGRAM/assets/120232371/721fc17c-6ce9-4d71-9609-9562ff6f80a8)

### Histogram of Color Image
![color histogram](https://github.com/Jayakrishnan22003251/HISTOGRAM/assets/120232371/f2337200-449c-4bc7-b259-e048c41fbbec)

### Histogram of Pixel intensities
![pixel histo](https://github.com/Jayakrishnan22003251/HISTOGRAM/assets/120232371/4a0a514d-4806-43c9-a16c-31a49ec31cc5)



### Histogram of Grayscale Image and any channel of Color Image
![gray histogram](https://github.com/Jayakrishnan22003251/HISTOGRAM/assets/120232371/1af8c37c-e00b-40ce-936c-d1bc2b87d5fe)
![rch](https://github.com/Jayakrishnan22003251/HISTOGRAM/assets/120232371/cca8dc69-949f-4195-ba1a-59f4bd08101a)

### Histogram Equalization of Grayscale Image

![c3](https://github.com/Jayakrishnan22003251/HISTOGRAM/assets/120232371/545c87b1-de31-435a-8c46-5683c6bb8ef0)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
