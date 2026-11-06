# EXP. 6 – EDGE DETECTION USING OPENCV

## NAME:  THARSHINI M
## REG NO: 212224230287

## Aim

To implement different edge detection techniques using OpenCV and Python to identify edges and boundaries in an image.

## Software Requirements

- Python
- Anaconda
- Jupyter Notebook
- OpenCV
- NumPy
- Matplotlib

## Edge Detection Techniques

1. Sobel Edge Detection
2. Laplacian Edge Detection
3. Canny Edge Detection

## Algorithm

1. Import the required libraries: OpenCV, NumPy, and Matplotlib.
2. Read the input image using `cv2.imread()`.
3. Convert the input image into grayscale.
4. Display the original image.
5. Apply Sobel edge detection in horizontal and vertical directions.
6. Combine both Sobel gradients using `cv2.magnitude()`.
7. Apply Laplacian edge detection using `cv2.Laplacian()`.
8. Apply Canny edge detection using `cv2.Canny()`.
9. Display all the edge-detected images separately.
10. Compare the results of different edge detection techniques.

## Implementation

### 1. Import Libraries

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

### 2. Read and Convert the Image

```python
image = cv2.imread('Image.png')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```

### 3. Display Original Image

```python
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

## OUTPUT:
<img width="177" height="244" alt="{C1978F5A-4CB4-4ADF-A07D-73B9FF9E6936}" src="https://github.com/user-attachments/assets/a18e05e9-c1c3-4dd6-9a87-1f8a65613cdf" />


### 4. Sobel Edge Detection

```python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)

sobel_combined = cv2.magnitude(sobel_x, sobel_y)

plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```

## OUTPUT:
<img width="171" height="242" alt="{202251F7-68AA-4BA6-B827-F8B91366B6E0}" src="https://github.com/user-attachments/assets/334d1593-f2c8-41fd-b8e0-f30f26154329" />


### 5. Laplacian Edge Detection

```python
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)

plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```

## OUTPUT;
<img width="195" height="273" alt="{843E9A74-9845-460A-B52F-F11947E75C95}" src="https://github.com/user-attachments/assets/083d5843-3acb-4156-ae3f-991a9d11ce08" />


### 6. Canny Edge Detection

```python
canny_edges = cv2.Canny(gray_image, 50, 150)

plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```

## Output:
<img width="192" height="267" alt="{1C0289F7-85B7-442B-997E-321D46A0F803}" src="https://github.com/user-attachments/assets/ac18dc3f-83c4-482b-8bb5-807afb17ef7b" />


## Result

Thus, Sobel, Laplacian, and Canny edge detection techniques were successfully implemented using OpenCV and Python. Each technique detects image edges differently and helps identify important boundaries and features.
