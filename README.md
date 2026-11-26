# DIPT-Ex--8
# Image Segmentation Using Thresholding Techniques in OpenCV

## Aim

To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

- Global Thresholding
- Adaptive Thresholding
- Otsu's Thresholding

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Load the input image using OpenCV.

### Step 3:

Convert the input image into grayscale format.

### Step 4: Global Thresholding

- Select a fixed threshold value.
- Apply thresholding to separate foreground and background pixels.
- Display the thresholded image.

### Step 5: Adaptive Thresholding

- Compute threshold values for small regions of the image.
- Apply Adaptive Mean Thresholding.
- Apply Adaptive Gaussian Thresholding.
- Display the segmented images.

### Step 6: Otsu's Thresholding

- Automatically determine the optimal threshold value.
- Apply Otsu's thresholding technique.
- Display the segmented image.

### Step 7:

Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program

## Developed By

**Name:** Nishma Sherin.K

**Register No:** 212224240104

## program:

### Original Grayscale Image:

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('HenryCavill.webp')  # Replace with your image file path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY) 
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert from BGR to RGB for display
plt.title("Original Image")
plt.axis('off')
```

### Global Thresholding:
```
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```


### Adaptive Thresholding:
```
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```

### Otsu's Thresholding:
```
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')

# Show the plot
plt.tight_layout()
plt.show()
```

## Output:

### Original Grayscale Image:

<img width="227" height="154" alt="image" src="https://github.com/user-attachments/assets/0176dd5d-c6cf-400c-81b7-304c75f0cc37" />

### Global Thresholding:

<img width="423" height="372" alt="image" src="https://github.com/user-attachments/assets/ecbbf626-6506-4fe4-a7cc-ec5cad5855f9" />


### Adaptive Thresholding:

<img width="430" height="364" alt="image" src="https://github.com/user-attachments/assets/0cafb8ec-955a-483d-b16b-94f0d67e3969" />

### Otsu's Thresholding:

<img width="466" height="361" alt="image" src="https://github.com/user-attachments/assets/63a8977c-e045-4cb1-be6e-23652dc516a9" />



## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
