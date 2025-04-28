# 2D Transformations on Images – Computer Vision Practical

## Overview

This project involves implementing basic **2-D geometric transformations** on images using programming techniques. The following transformations are applied individually to images:

- **Translation**
- **Rotation**
- **Scaling**
- **Shearing**
- **Reflection**

These transformations are fundamental operations in computer vision, image processing, and graphics.

---

## Requirements

- Python 3.x
- OpenCV (`cv2`) library
- NumPy (`numpy`)

You can install the necessary packages using:

```bash
pip install opencv-python numpy
```

---

## How to Run

1. Clone or download this repository.
2. Place the input images in the specified directory (or the working directory).
3. Run the individual Python programs for each transformation or a combined script that offers a menu-based interface.

Example to run:

```bash
python translation.py
```

or for the combined program:

```bash
python transformations.py
```

---

## Transformations Implemented

### 1. Translation
- Shifts the image by a specified distance along the X and Y axes.

### 2. Rotation
- Rotates the image by a specified angle about its center.

### 3. Scaling
- Resizes the image by given scaling factors along X and Y axes.

### 4. Shearing
- Applies shearing along X and/or Y axes to distort the image shape.

### 5. Reflection
- Flips the image along X-axis, Y-axis, or both.

---

## File Structure

```
/2D_Transformations
    ├── translation.py
    ├── rotation.py
    ├── scaling.py
    ├── shearing.py
    ├── reflection.py
    ├── transformations.py   # (Optional) Combined menu-driven program
    └── input_image.jpg
```

---

## Sample Usage

Each script reads an input image, applies the specified transformation, and displays the original and transformed images side-by-side.

Example (Translation):

```python
import cv2
import numpy as np

img = cv2.imread('input_image.jpg')
rows, cols = img.shape[:2]

M = np.float32([[1, 0, 100], [0, 1, 50]])
translated_img = cv2.warpAffine(img, M, (cols, rows))

cv2.imshow('Original', img)
cv2.imshow('Translated', translated_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

---

## Notes

- Ensure that the input image file path is correct.
- Adjust transformation parameters (like translation distance, rotation angle, scale factor, shear factor) in the scripts as needed.
- Save the output images if required using `cv2.imwrite()`.

---





