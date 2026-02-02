# ============ HISTORICAL COLORIZATION PROJECT REPORT  ============


# Internship Project Report

## Project Title:
Historical Photo Colorization Using Python

Student Name: Mehkaan Anjum  
Course: BCA  

---

## 1. Project Overview
This project demonstrates a basic historical photo colorization technique using Python.
The program allows users to upload a black and white historical image and generate a
colorized version based on a selected historical period such as 1920s or World War II (WWII).

The project focuses on fundamental image processing concepts and is designed for
academic and internship submission.

---

## 2. Objectives
- Convert black and white historical images into colored images
- Apply period-based color tones such as 1920s and WWII
- Understand grayscale to RGB conversion
- Perform pixel-level image manipulation
- Display and save processed images

---

## 3. Tools and Libraries
- Python 3.x
- Google Colab
- NumPy
- Pillow (PIL)
- Matplotlib

---

## 4. Methodology

1. Image Upload  
The user uploads a black and white historical image using Google Colab file upload.

2. Image Loading  
The uploaded image is opened and converted to RGB format using the Pillow library.

3. Grayscale Conversion  
The RGB image is converted into grayscale to obtain intensity values.

4. Array Conversion  
The grayscale image is converted into a NumPy array for pixel processing.

5. Base Colorization  
A base color image is created by generating RGB channels from grayscale values.

6. Historical Period Selection  
The program supports two periods:
- 1920s (warm sepia tones)
- WWII (muted green tones)

7. Period-Based Adjustment  
Color intensities are modified based on the selected historical period.

8. Pixel Clipping  
Pixel values are clipped between 0 and 255 to maintain valid image data.

9. Image Reconstruction  
The processed array is converted back into an image format.

10. Output Generation  
The final colorized image is saved as historical_colorized_output.jpg.

11. Result Display  
Original, grayscale, and colorized images are displayed for comparison.

---

## 5. Output Description
The output includes a colorized historical image saved in JPEG format and
a visual comparison of all image stages.

---

## 6. Observations and Limitations
- Colorization is rule-based and not AI-based
- Colors are approximate and for learning purposes
- Image quality affects output results

---

## 7. Future Enhancements
- Add more historical periods
- Improve color accuracy
- Introduce interactive selection options

---

## 8. Conclusion
This project demonstrates how basic image processing techniques can be used
to apply color effects to historical black and white images using Python.

---

## 9. Author
Mehkaan Anjum  
BCA student 
