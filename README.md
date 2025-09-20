Brain Tumor Detection using Image Processing

This project demonstrates how classical image processing techniques can be used to detect brain tumors in MRI scans. Instead of relying on deep learning, it applies filters, thresholding, and morphological operations (using OpenCV, NumPy, Matplotlib) to extract and highlight tumor regions.


It was originally written in a Jupyter Notebook and later converted into a Python script (brain_tumor_detection_cleaned.py) for easier execution.
Introduction
Brain tumor detection is an important step in medical diagnosis. While deep learning approaches exist, this project shows how classical image processing can still achieve meaningful results.

The script performs:
Preprocessing of MRI scans (noise removal, intensity adjustment).
Morphological operations to enhance tumor boundaries.
Thresholding to separate tumor from background.
Contour detection to highlight and measure the tumor.
The output is an annotated MRI image with the detected tumor marked in green contour lines, along with the area and perimeter of the tumor.


Features

✔️ Load MRI brain images in grayscale
✔️ Histogram analysis to understand pixel intensity distribution
✔️ Noise reduction with Gaussian blur and median filtering
✔️ Morphological gradient, opening, closing, erosion, dilation
✔️ Thresholding to isolate tumor region
✔️ Tumor detection via contour finding
✔️ Outputs tumor area and perimeter
✔️ Visualization using Matplotlib

Requirements:

* The project needs Python 3.8+ and the following libraries:
* opencv-python → Image processing
* numpy → Array and matrix operations
* matplotlib → Plotting images and histograms
* scikit-image (optional) → Extra image processing functions
* scipy (optional) → Scientific computing utilities
* jupyter (optional) → If you want to run this in notebooks
* See requirements.txt for exact package list.


Installation

Clone this repository:
git clone https://github.com/YOUR_USERNAME/brain-tumor-detection.git
cd brain-tumor-detection

Install dependencies:
pip install -r requirements.txt


Usage

Place your MRI image in the project folder.

Run the script:
python brain_tumor_detection_cleaned.py


The script will:
Preprocess the image.
Segment potential tumor regions.
Show step-by-step plots of each stage.
Print Area and Perimeter if a tumor is detected.
Display the detected tumor contour in green.


Working Pipeline

1. Here’s what happens inside the script step by step:
2. Load Image → MRI image is loaded in grayscale.
3. Histogram Analysis → Pixel intensity distribution checked.
4. First Enhancement → Gaussian blur + intensity adjustment.
5. Noise Removal → Median filtering applied.
6. Morphological Gradient → Highlights edges.
7. Second Enhancement → Combine gradient with denoised image.
8. Thresholding → Convert to binary (tumor vs. non-tumor).
9. Morphological Operations → Opening, closing, erosion, dilation to refine tumor region.
10. Masking → Apply mask to original image.
11. Final Enhancement & Thresholding → Isolate tumor more clearly.
12. Contour Detection → Find tumor shape, calculate area and perimeter, draw it in green.


Future Improvements

Support for multiple MRI images at once.
Add deep learning (CNN-based) tumor detection for comparison.
Save results (tumor masks & contour images) automatically.
Create a simple Streamlit Web App for user-friendly uploads.
