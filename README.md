# Optimizing ALPR Performance Through Adaptive Image Processing Techniques
Automatic License Plate Recognition (ALPR) is a vital component in intelligent transportation systems, such as traffic management, toll collection, and law enforcement. This project aims to optimize the performance of ALPR systems by proposing and evaluating three adaptive image processing techniques. The second method was chosen as the most effective for enhancing recognition accuracy under various lighting conditions and environmental challenges.

## Image Processing Techniques
The following image processing methods were tested and compared based on their impact on ALPR performance:

### Method 1
- **Image Enlargement:** No enlargement
- **Basic Thresholding Operation:** Thresholding to zero
- **Adaptive Thresholding Operation:** No adaptive thresholding
- **Morphological Operation:** Morphological opening and dilation used
- **OCR Recognition Time:** Fastest
- **Character Recognition Performance:** Generally identifiable, but with occasional multiple predictions
- **Total Processing Time:** 3.95 seconds per image

### Method 2 (Chosen as the Most Effective)
- **Image Enlargement:** ESPCN model with a factor of 3
- **Basic Thresholding Operation:** No thresholding
- **Adaptive Thresholding Operation:** Adaptive thresholding using Gaussian Mean
- **Morphological Operation:** Morphological opening used
- **OCR Recognition Time:** Slower than Method 1, but faster than Method 3
- **Character Recognition Performance:** Accurate recognition for each character without ambiguity
- **Total Processing Time:** 5.06 seconds per image

### Method 3
- **Image Enlargement:** ESPCN model with a factor of 3
- **Basic Thresholding Operation:** No thresholding
- **Adaptive Thresholding Operation:** Adaptive thresholding using Gaussian Mean
- **Morphological Operation:** Morphological opening used
- **OCR Recognition Time:** Slowest
- **Character Recognition Performance:** Some characters exhibit difficulty in recognition, leading to decreased accuracy
- **Total Processing Time:** 4.82 seconds per image

### Conclusion
From the comparison table, Method 2 emerged as the most effective, balancing high accuracy with reasonable processing times. This method produced the best results for clear and accurate character recognition, making it the optimal choice for the proposed ALPR system.

---

## Real-Life Verification
To assess the effectiveness of Method 2 in real-world scenarios, we conducted verification with 20 images for each of the following four conditions:

1. **Daytime with Clear Visibility**
2. **Daytime with Visible Characters**
3. **Nighttime with Normal Light**
4. **Nighttime with Strong Light**

The results demonstrated that Method 2 consistently provided high-quality recognition, even under challenging lighting conditions.

---

## Performance Analysis
The analysis of ALPR system performance, highlighting the impact of environmental factors on license plate recognition accuracy. The second method, with its adaptive image processing flow, was particularly effective in enhancing character clarity and distinguishing them from backgrounds.

### Scenario 1: Daytime with Clear Visibility
- The ALPR system achieved 100% detection accuracy in optimal lighting conditions, successfully identifying the rear license plate. The application of Method 2 resulted in 100% detection and a character recognition accuracy of 99.96%.

### Scenario 2: Daytime with Visible Characters
- In this scenario, visibility issues, such as dirt on the license plate, affected the quality of the image. Despite these challenges, Method 2 successfully clarified the characters, achieving 100% detection and 99.89% character accuracy.

### Scenario 3: Nighttime with Normal Light
- The system performed well in nighttime conditions, where visibility was reduced. Method 2 enabled the system to detect and recognize license plates with 100% accuracy, although character recognition accuracy slightly dropped due to the dimmer environment and truck lights.

### Scenario 4: Nighttime with Strong Lights
- In this scenario, the strong backlight from the vehicle made license plate recognition difficult. Despite the challenges, Method 2 successfully detected and recognized the license plate, achieving 100% detection and effective segmentation of characters.

These results underscore the effectiveness of Method 2, even in challenging lighting and environmental conditions. The system demonstrated its robustness in detecting and recognizing license plates across a wide range of scenarios.

---

## Conclusion
This project successfully developed and evaluated an adaptive image processing technique to optimize the performance of ALPR systems. The comparison of various image processing techniques highlighted that Method 2 significantly improved character recognition accuracy by utilizing Adaptive Thresholding Gaussian Mean and AI-based image enlargement. The system performed well across diverse environmental conditions, such as varying light levels, background noise, and dirt presence on the license plate.

Despite the successes, the evaluation revealed that factors such as the spacing between characters, background noise, and the surrounding lighting conditions can significantly impact the accuracy of the system. These findings suggest that further optimization is necessary to make ALPR systems more robust in real-world conditions.

Future research could explore the application of alternative neural network architectures or new image processing techniques to further enhance the robustness and reliability of ALPR systems.

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

## Project Structure

The repository is organized as follows:

ALPR-Optimization/ │ ├── README.md # Project overview, setup, and usage instructions ├── requirements.txt # List of dependencies and libraries ├── dataset/ # Folder to store or link to dataset files │ ├── images/ # Folder with the image data │ └── dataset_split/ # Split dataset (training, testing, validation) ├── src/ # Folder for source code │ ├── image_processing/ # Scripts related to image processing (Method 1, 2, 3) │ ├── model/ # Model-related code (training, testing, etc.) │ ├── utils/ # Helper functions, utilities │ └── main.py # Main script to run the ALPR system ├── results/ # Folder to store results, outputs, or logs │ ├── images/ # Processed images, detection results │ └── evaluation/ # Evaluation metrics or logs ├── docs/ # Optional folder for detailed documentation (e.g., papers) │ ├── conference_paper.pdf │ └── fyp_report.pdf 

---


### Explanation:

- **`README.md`**: Provides an overview of the project, setup instructions, and usage details.
- **`requirements.txt`**: Contains a list of dependencies required to run the project. To install the necessary dependencies, run:
  ```bash
  pip install -r requirements.txt

- **`dataset/`**: Contains the image dataset used for training and testing the ALPR system. It is split into three parts: `training`, `testing`, and `validation`. Due to privacy reasons, the dataset is not included in the repository, but a link to access it can be found [here](link_to_dataset).
- **`src/`**: This directory contains the source code for the ALPR system.
- **`image_processing/`**: Scripts implementing the image processing techniques (Method 1, Method 2, etc.).
- **`model/`**: Code related to the model's training, testing, and evaluation processes.
- **`utils/`**: Helper functions and utilities used across the codebase.
- **`main.py`**: The main script to run the ALPR system and execute all steps in the workflow.
- **`results/`**: Contains results, including processed images, output logs, and evaluation metrics.
- **`images/`**: Processed images and detection results.
- **`evaluation/`**: Files related to performance evaluation, such as accuracy metrics or logs.
- **`conference_paper.pdf`**: The conference paper for the ALPR system.
- **`fyp_report.pdf`**: Final Year Project report.



## Limitations
- The trained AI model is not included due to confidentiality agreements with the collaborating company.
- The system's performance may vary depending on regional datasets and environmental conditions.
- Further optimization is required for complex traffic scenarios, such as crowded areas or multiple vehicles in the frame.


## Disclaimer
Due to confidentiality agreements, certain proprietary components (e.g., AI models) are excluded from this repository.

## Acknowledgments
This project was completed as part of my Final Year Project at UCSI University, Malaysia. Special thanks to my supervisor, Dr Mohammad Arif Bin Ilyas, and Billion Prima Sdn Bhd for their guidance and support.

