# Vietnamese License Plate Recognition

## Project Summary
This project focuses on automating license plate recognition for Vietnamese vehicles using image processing techniques and machine learning. With the increasing number of vehicles on the road, manual vehicle management in parking lots becomes inefficient. This project aims to provide a robust and automated solution using OpenCV and K-Nearest Neighbor (KNN) algorithm to recognize license plates from images.

## Table of Contents
1. Introduction
2. Overview of License Plate Recognition
3. License Plate Detection & Segmentation
4. Character Segmentation
5. Character Recognition
6. Performance Evaluation
7. Conclusion and Future Development

## 1. Introduction
### Overview
The project involves:
- Understanding license plate recognition systems
- Studying image processing techniques
- Implementing a system to detect and recognize Vietnamese license plates

### Tasks
- Implementing image processing techniques for license plate recognition
- Training a machine learning model for character recognition
- Evaluating performance and optimizing the system

## 2. Overview of License Plate Recognition
### License Plate Concept
Vietnamese license plates are standardized metal plates with region-based numerical and alphabetical identifiers. The project sets parameters for detecting and filtering valid license plates.

### Image Processing & OpenCV
Image processing is used to enhance image quality, recognize objects, and extract features. OpenCV is a powerful library used for:
- Image recognition
- Edge detection
- Feature extraction

### Solution Approach
1. Detect license plate location
2. Segment characters from the plate
3. Recognize characters and convert to ASCII

## 3. License Plate Detection & Segmentation
### Image Preprocessing
- Convert images to grayscale
- Increase contrast using morphological operations (Top Hat & Black Hat)
- Reduce noise using Gaussian filters
- Apply adaptive thresholding for binary conversion
- Detect edges using the Canny algorithm
- Identify contours to locate license plates

## 4. Character Segmentation
### Process
- Rotate license plate images for proper alignment
- Identify and extract character regions
- Filter out irrelevant noise

## 5. Character Recognition
### Machine Learning Approach
- K-Nearest Neighbor (KNN) algorithm is used for classification
- Training dataset includes labeled characters from Vietnamese plates
- The model recognizes characters and outputs ASCII results

## 6. Performance Evaluation
### Testing Methodology
- Input images from a Samsung J7 Prime camera (FHD 1920x1080, 9.6MP, 8fps)
- Process frames for license plate detection and recognition
- Evaluation based on:
  - License plate detection rate
  - Character recognition accuracy

### Results
| Plate Type | Total Plates | Plates Found | Detection Rate |
|------------|--------------|--------------|---------------|
| Single-row | 370 | 182 | 49.2% |
| Two-row | 2349 | 924 | 39.3% |

| Plate Type | Plates Found | Correct | 1 Char Wrong | 2+ Chars Wrong |
|------------|--------------|--------|--------------|----------------|
| Single-row | 182 | 61 (33.5%) | 88 (48.4%) | 33 (18.1%) |
| Two-row | 924 | 286 (31.0%) | 273 (29.5%) | 365 (39.5%) |

## 7. Conclusion and Future Development
### Key Findings
- The KNN-based recognition model is lightweight and simple but has limitations with noise and reflections.
- Accuracy is affected by lighting conditions and background noise.

### Future Improvements
- Implement advanced machine learning models like CNN or YOLO for higher accuracy.
- Use specialized cameras for better image quality.
- Enhance preprocessing techniques to reduce noise and improve segmentation.
- Integrate with vehicle management systems for broader applications.

## References
Refer to the full report for detailed references on methodologies, algorithms, and datasets.

