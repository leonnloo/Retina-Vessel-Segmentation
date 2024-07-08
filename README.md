# 👁️ Retina Vessel Segmentation

<p align="center">
  <img src="https://github.com/leonnloo/Retina-Vessel-Segmentation/assets/88762191/a50a4a02-4859-492b-9359-ba82219e93ce" alt="EyeGIF">
</p>


Welcome to the Retina Vessel Segmentation repository! This project focuses on the segmentation of blood vessels in retinal images using advanced image processing techniques. 
The goal is to aid in the diagnosis and treatment of various eye diseases by providing accurate and reliable vessel segmentation.

## 🩺 Introduction

Precise segmentation of blood vessels in retinal images is crucial for diagnosing and preventing diseases such as glaucoma, hypertension, and diabetes. This project aims to automate the segmentation process to reduce human errors and improve the accuracy of medical diagnoses.

## 📝 Algorithm Design

The segmentation process involves several steps:

1. **Image Conversion**: The raw image is converted to the green color channel, which has higher contrast between the vessels and the retina. This channel is then converted to grayscale using Contrast Limited Adaptive Histogram Equalization (CLAHE) for enhanced contrast.

2. **Gaussian Smoothing**: Applied to reduce noise and blur irrelevant high-frequency details, improving the clarity of vessel structures.

3. **Top-Hat Enhancement**: Enhances small, dark vessels against the lighter background of the retina using morphological closing.

4. **Contrast Enhancement**: Further increases the visibility of vessels using adaptive histogram equalization.

5. **CDF Thresholding**: Converts the enhanced grayscale image to a binary image, separating vessels from the background based on pixel intensity distribution.

6. **Hysteresis Thresholding**: Applies two thresholds to ensure edge continuity and reduce noise, generating a binary image of the retina vessels.

7. **Morphological Closing**: Closes small gaps and holes within the detected vessels for a more accurate segmentation.

8. **Binary Image Combination**: Combines the outputs of CDF and hysteresis thresholding to improve segmentation quality.

## 📊 Results

The performance of the segmentation process was evaluated across 20 retinal images, with the following average metrics:

- **Precision (P)**: 69.12%
- **Negative Predictive Value (N)**: 98.13%
- **Total Accuracy (T)**: 94.40%

These results demonstrate the model's effectiveness in accurately detecting retinal vessels.


## 🔧 How to Run the Code

1. Open the file using Jupyter Notebook.
2. The python version used was 3.11.8.
3. Install the required libraries:
   
   ```bash
   pip install opencv-python scikit-image
