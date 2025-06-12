# Image Processing 
This project implements a comprehensive image processing pipeline to perform component extraction, enhancement of blurry images, noise removal, and visual enhancement of challenging images. It processes various types of images, including circles, COVID-19 visualizations, buildings, dogs, wind charts, rockets, text, newspapers, and nameplates. The project uses OpenCV, NumPy, Matplotlib, and other Python libraries to achieve these tasks and generates a detailed HTML report summarizing the techniques, results, and findings.

## Table of Contents

Project Overview
Tasks and Techniques
Component Extraction
Enhancement of Blurry Images
Noise Removal
Text Enhancement
Visual Enhancement of Challenging Images


## Installation
Usage
File Structure
Dependencies
Output
Limitations
Future Improvements
License


## Project Overview
The project focuses on processing a set of images to achieve specific objectives:

Component Extraction: Detect and isolate specific components (circles, colored parts of a COVID-19 visualization).
Enhancement of Blurry Images: Improve clarity and sharpness of blurry images (e.g., buildings, dogs).
Noise Removal: Reduce noise in images (e.g., wind charts, rockets).
Text Enhancement: Enhance readability of noisy text images.
Visual Enhancement of Challenging Images: Improve visibility of complex images ( newspapers, nameplates).

The pipeline processes images using a variety of computer vision techniques, including Hough Transform, color segmentation, K-means clustering, Wiener filtering, unsharp masking, CLAHE, and morphological operations. A detailed HTML report is generated to document the techniques used, results, pros and cons, quality achieved, failure reasons, and suggestions for future improvements.

Tasks and Techniques
Component Extraction

Circle Detection:
Technique: Hough Circle Transform with Gaussian blur and Canny edge detection.
Image: 7 circles.png.
Purpose: Detect circular patterns in the image.


COVID Component Extraction:
Techniques: Color segmentation in HSV space, contour detection, K-means clustering.
Image: Multi_objects_separation.jpeg.
Purpose: Isolate different colored components of a COVID-19 visualization.



Enhancement of Blurry Images

Building Enhancement:
Techniques: Unsharp masking, Laplacian sharpening, frequency domain high-pass filtering.
Image: Building.jpg.
Purpose: Improve clarity and edge definition of a blurry building image.


Dog Image Enhancement:
Techniques: Wiener filtering for motion deblurring, unsharp masking, CLAHE contrast enhancement.
Image: Dog.jpeg.
Purpose: Reduce motion blur and enhance details in a dog image.



Noise Removal

Wind Chart Enhancement:
Techniques: Gaussian filtering, median filtering, bilateral filtering, adaptive thresholding, morphological operations.
Image: Noisy_1.png.
Purpose: Remove noise and improve visibility of wind chart details.


Rocket Image Denoising:
Techniques: Non-local means denoising, wavelet denoising, median filtering, bilateral filtering.
Image: Rocket.jpeg.
Purpose: Reduce noise while preserving structural details of a rocket image.



Text Enhancement

Noisy Text Enhancement:
Techniques: Median filtering, adaptive thresholding, morphological operations, Otsu's thresholding, CLAHE contrast enhancement.
Image: Text.jpeg.
Purpose: Improve readability of noisy text.



Visual Enhancement of Challenging Images

Newspaper Enhancement:
Techniques: CLAHE contrast enhancement, unsharp masking, non-local means denoising, Otsu's binarization, adaptive thresholding, morphological operations.
Image: Noisy_2.jpg.
Purpose: Enhance readability of a noisy newspaper image.


Nameplate Enhancement:
Techniques: CLAHE contrast enhancement, kernel sharpening, non-local means denoising, adaptive thresholding, Otsu's thresholding, morphological operations.
Image: Name plate.jpg.
Purpose: Improve visibility of text on a nameplate.




# Installation
To set up the project, follow these steps:

Clone the Repository (if applicable):
git clone <repository_url>
cd image-processing-project


Install Dependencies:Ensure you have Python 3.8+ installed. Install the required packages:
pip install -r requirements.txt


Install Additional Libraries:Install PyWavelets for wavelet denoising:
pip install PyWavelets


Prepare Input Images:Place the following images in the /content/ directory:

7 circles.png
Multi_objects_separation.jpeg
Building.jpg
Dog.jpeg
Noisy_1.png
Rocket.jpeg
Text.jpeg
Noisy_2.jpg
Name plate.jpg


## Set Up Environment:

Ensure a Jupyter Notebook or Google Colab environment is available for visualization.
Verify that all image paths are correctly specified in the code.




## Usage

Run the Image Processing Pipeline:

Execute the main script to process all images:image_paths = {
    'circle': '/content/7 circles.png',
    'covid': '/content/Multi_objects_separation.jpeg',
    'buildings': '/content/Building.jpg',
    'dog': '/content/Dog.jpeg',
    'wind_chart': '/content/Noisy_1.png',
    'rocket': '/content/Rocket.jpeg',
    'noisy_text': '/content/Text.jpeg',
    'newspaper': '/content/Noisy_2.jpg',
    'nameplate': '/content/Name plate.jpg'
}
process_all_images(image_paths)


This will process each image using the corresponding techniques and save the results.


Generate the HTML Report:

Run the report generation function to create and display the HTML report:display_report()


The report will be saved as image_processing_report.html and opened in a new browser tab.


View Results:

Processed images are saved in the working directory (circle_processed.jpg, buildings_enhanced.jpg).
The HTML report includes original and processed images, techniques used, and detailed discussions.





## Dependencies
The project requires the following Python packages:
opencv-python
numpy
matplotlib
scikit-learn
pywavelets
base64
ipython

Install them using:
pip install opencv-python numpy matplotlib scikit-learn pywavelets ipython


## Output

Processed Images: Saved in the working directory with descriptive filenames (e.g., circle_processed.jpg, dog_enhanced.jpg).
HTML Report: A comprehensive report (image_processing_report.html) that includes:
Original and processed images (encoded in base64).
Techniques used for each task.
Python code snippets.
Discussion of results, including pros, cons, quality achieved, failure reasons, and suggestions for future processing.
Visual comparisons of original and processed images.



The report is styled with CSS for readability and includes sections for each task, making it easy to navigate and understand the results.




