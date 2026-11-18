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

**Name:** RAMKUMAR S

**Register No:** 212225240115

## Output

### Original 
```
import cv2
import matplotlib.pyplot as plt

img = cv2.imread("criket.webp")

if img is None:
    print("Error: Image not found. Check the file path.")
else:
    img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
    plt.imshow(img_rgb)
    plt.title("Original Image")
    plt.axis("off")
    plt.show()
```
<img width="526" height="350" alt="image" src="https://github.com/user-attachments/assets/f5cf89f7-fb36-49d9-8da6-f8fa32ab5f70" />

### Original Grayscale Image
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("criket.webp", cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap="gray")
plt.title("Original Grayscale Image")
plt.axis("off")
plt.show()
```
<img width="515" height="352" alt="image" src="https://github.com/user-attachments/assets/557ae7fc-e53a-49b2-a6c0-a7761918af74" />

### Global Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("criket.webp", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(img, 127, 255, cv2.THRESH_BINARY)
plt.imshow(result, cmap="gray")
plt.title("Global Thresholding")
plt.axis("off")
plt.show()
```
<img width="513" height="322" alt="image" src="https://github.com/user-attachments/assets/eccd0dc3-0a93-4f05-93f3-4b163453691d" />


### Adaptive Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("criket.webp", cv2.IMREAD_GRAYSCALE)
result = cv2.adaptiveThreshold(
    img, 255,
    cv2.ADAPTIVE_THRESH_GAUSSIAN_C,
    cv2.THRESH_BINARY,
    11, 2
)
plt.imshow(result, cmap="gray")
plt.title("Adaptive Thresholding")
plt.axis("off")
plt.show()
```
<img width="506" height="334" alt="image" src="https://github.com/user-attachments/assets/3e06893f-4d19-4d7e-9f76-8341b9b1b0c7" />

### Otsu's Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("criket.webp", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(
    img, 0, 255,
    cv2.THRESH_BINARY + cv2.THRESH_OTSU
)
plt.imshow(result, cmap="gray")
plt.title("Otsu's Thresholding")
plt.axis("off")
plt.show()
```
<img width="493" height="333" alt="image" src="https://github.com/user-attachments/assets/62fd14e8-c0c4-4b04-af8b-114844662222" />


## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
