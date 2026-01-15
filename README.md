# Historical-colorization-
ColorizationHISTORICAL PHOTO COLORIZATION (NO ERRORS)
# ==============================================

!pip install -q pillow matplotlib numpy opencv-python

import cv2
import numpy as np
import matplotlib.pyplot as plt
from PIL import Image
from google.colab import files

# -------------------------------
# Upload black & white photo
# -------------------------------
print("Upload a BLACK & WHITE historical photo")
uploaded = files.upload()
img_path = list(uploaded.keys())[0]

# Read image
img = cv2.imread(img_path)
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# -------------------------------
# Choose historical period
# -------------------------------
print("\nChoose Historical Period")
print("1 - 1920s")
print("2 - World War II")
print("3 - 1970s")
print("4 - Modern")

choice = input("Enter choice: ")

# Color maps for different eras
if choice == "1":      # 1920s
    colormap = cv2.COLORMAP_PINK
elif choice == "2":    # WWII
    colormap = cv2.COLORMAP_BONE
elif choice == "3":    # 1970s
    colormap = cv2.COLORMAP_OCEAN
else:
    colormap = cv2.COLORMAP_JET

# -------------------------------
# Apply colorization
# -------------------------------
colorized = cv2.applyColorMap(gray, colormap)

# -------------------------------
# Save Output
# -------------------------------
cv2.imwrite("historical_colorized.png", colorized)

# -------------------------------
# Show Result
# -------------------------------
plt.figure(figsize=(12,5))
plt.subplot(1,2,1)
plt.title("Original (B&W)")
plt.imshow(gray, cmap='gray')
plt.axis("off")

plt.subplot(1,2,2)
plt.title("Historical Colorized")
plt.imshow(cv2.cvtColor(colorized, cv2.COLOR_BGR2RGB))
plt.axis("off")

plt.show()

files.download("historical_colorized.png") 
