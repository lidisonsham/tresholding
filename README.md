# Ex 08: image-thresholding-opencv
# Aim
To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

Global Thresholding Adaptive Thresholding Otsu's Thresholding

# Software Used
Anaconda – Python 3.7 Jupyter Notebook / VS Code OpenCV (cv2) NumPy Matplotlib

# Algorithm
Step 1:Import the required libraries: OpenCV, NumPy, and Matplotlib.

Step 2:Load the input image using OpenCV.

Step 3:Convert the input image into grayscale format.

Step 4: Global Thresholding Select a fixed threshold value. Display the thresholded image.

Step 5: Adaptive Thresholding Compute threshold values for small regions of the image. Apply Adaptive Mean Thresholding. Apply Adaptive Gaussian Thresholding. Display the segmented images.

Step 6: Otsu's Thresholding Automatically determine the optimal threshold value. Apply Otsu's thresholding technique. Display the segmented image.

Step 7: Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

# Program

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('pic8')  # Replace with your image file path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)  # Convert to grayscale
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert from BGR to RGB for display
plt.title("Original Image")
plt.axis('off')
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')

# Adaptive Thresholding
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')

# Otsu's Method
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')

# Show the plot
plt.tight_layout()
plt.show()

```
# Output
<img width="996" height="335" alt="image" src="https://github.com/user-attachments/assets/28a573cf-eb8a-436e-8c57-610c4522a8c4" />
<img width="1018" height="358" alt="image" src="https://github.com/user-attachments/assets/3f20b4d9-2885-4745-841e-f04105048393" />
<img width="1122" height="338" alt="image" src="https://github.com/user-attachments/assets/d1637f1e-c5fc-40ee-8c79-dbcf1f71c512" />
<img width="1078" height="342" alt="image" src="https://github.com/user-attachments/assets/a6c14f50-6cf5-4500-b910-89a7a66f3f1a" />
<img width="1086" height="352" alt="image" src="https://github.com/user-attachments/assets/289fdac9-b23b-4db2-9e0f-563b590de5f1" />
<img width="1050" height="345" alt="image" src="https://github.com/user-attachments/assets/17b7ffe0-3595-49d9-8792-a70c888923b4" />
<img width="1045" height="342" alt="image" src="https://github.com/user-attachments/assets/30c1fe42-43f4-4ff8-b26b-abbdf5202f1f" />
<img width="1020" height="357" alt="image" src="https://github.com/user-attachments/assets/958c44ad-2076-4205-9bb2-73e63d95d40d" />
<img width="1045" height="333" alt="image" src="https://github.com/user-attachments/assets/f5d4868f-3de8-49aa-8b9e-69acb6432d4b" />






# Result
Thus, image segmentation is successfully performed using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques in OpenCV.
