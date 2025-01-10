# ALPR Optimization Project

## Overview
This project focuses on optimizing image processing techniques for Automatic License Plate Recognition (ALPR) systems. It includes experiments with three different image processing methods, performance evaluation, and an analysis of their efficiency in license plate detection and recognition. The work is tailored for industrial use, specifically for rear-ended truck license plates in a cargo terminal setting.

## Key Features
- **Optimization Techniques**: Implemented and compared three image processing methods to enhance detection accuracy.
- **Performance Analysis**: Evaluated visibility, recognition rates, and processing time.
- **Real-World Dataset**: Used proprietary image data (not included in this repository for confidentiality).
- **Comprehensive Results**: Included processed images, evaluation metrics, and comparison tables.

## What's Included
1. **Source Code**: Scripts for image processing and optimization techniques.
2. **Results**: Processed images and performance metrics in an Excel sheet.
3. **Reports**: Final year project report, conference paper, and presentation slides.

---

## Tools and Technologies
This project used the following tools, libraries, and datasets to implement and test the ALPR system:

### **Software and IDE**
- **PyCharm:** Used as the Integrated Development Environment (IDE) for coding and debugging.

### **Libraries and Frameworks**
- **OpenCV:** For image processing tasks such as thresholding, morphological operations, and adaptive thresholding.
- **Tesseract OCR:** Used for Optical Character Recognition (OCR) to extract text from license plate images.
- **NumPy:** For numerical operations and matrix manipulations.
- **TensorFlow/Keras:** Utilized for AI-based image enlargement models (ESPCN).
- **Matplotlib:** For data visualization, including generating plots to assess recognition accuracy.

### **Datasets**
The dataset used in this project was generously provided by an industrial company, specifically tailored for use with the ALPR system in the industrial sector. It consists of a collection of images captured by cameras at a cargo terminal, focusing on rear-ended trucks with visible license plates. 

### **Hardware**
- **GPU (NVIDIA):** Used for faster processing of AI models and image enlargement.
- **Standard Camera Setup:** For capturing images of license plates under varying conditions (daytime, nighttime, strong backlight, etc.).

---

## Limitations
- The trained AI model is not included due to confidentiality agreements with the collaborating company.
- The system's performance may vary depending on regional datasets and environmental conditions.
- Further optimization is required for complex traffic scenarios, such as crowded areas or multiple vehicles in the frame.


## Disclaimer
Due to confidentiality agreements, certain proprietary components (e.g., AI models) are excluded from this repository.

## Acknowledgments
This project was completed as part of my Final Year Project at UCSI University, Malaysia. Special thanks to my supervisor, Dr Mohammad Arif Bin Ilyas, and Billion Prima Sdn Bhd for their guidance and support.

