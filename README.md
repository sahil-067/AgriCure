# AgriCure
# Plant Disease Detection App

## Overview

This repository contains the code and resources for an Web application designed to detect plant diseases using a multi-layered approach powered by YOLOv8. The application leverages three machine learning models to ensure accurate and efficient image processing:

1. **General Object Rejection Model:** Filters out images containing non-plant objects, such as humans, vehicles, or other unrelated elements.
2. **Plant Detection Model:** Identifies whether the input image contains a plant or if it is an invalid test case, such as a green screen or an unrelated object.
3. **Precision Plant Validation Model:** Confirms the presence of a plant and ensures that only high-confidence images (precision above 90%) proceed to disease detection.

The final output identifies plant diseases, aiding farmers in diagnosing issues efficiently.

---

## Key Features

- **Multi-layered Validation:** Ensures only relevant plant images are processed, improving accuracy.
- **Disease Detection:** Provides disease insights for the validated plant images.
- **Efficient Implementation:** Optimized using YOLOv8 for real-time performance.
- **Cross-Platform Compatibility:** Available as a lightweight Android application for use in resource-constrained environments.

---

## Technologies Used

- **YOLOv8:** Advanced object detection model for high precision and speed.
- **Programming Languages:**
  - HTML (53%)
  - Python (24%)
  - CSS (26%)

---

## Dataset

The app is based on research data involving bitter gourd leaves, focusing on:
- Diseases: Downy Mildew, Leaf Spot, Jassid
- Nutrient Deficiencies: Potassium, Magnesium, Nitrogen, and their combinations
- Healthy leaves for reference

Initial dataset: 785 images
Augmented dataset: 2,432 images

---

## Model Architecture

### General Object Rejection Model
- Filters out non-plant objects.
- Ensures the pipeline processes only images with potential plant content.

### Plant Detection Model
- Detects plants while rejecting unrelated objects or test cases (e.g., green screens).
- Acts as a secondary filter for enhanced validation.

### Precision Plant Validation Model
- Validates plant images passing prior tests.
- Applies a strict precision threshold (>75%) to eliminate low-confidence cases.

### Disease Detection Model
- Identifies diseases in the final validated plant images.
- Leverages YOLOv8 for high accuracy and low false positives.

---

## Performance Metrics

- **Mean Average Precision (mAP):** 92.9% at IoU=0.50
- **Precision:** 90%
- **Recall:** 87%
- **F1 Score:** 91.66%

---

## Usage

1. Launch the application on your device.
2. Upload an image through the interface.
3. Receive results:
   - If non-plant content is detected, the image is rejected.
   - If the image passes all layers, the app provides disease analysis.

---

## Contributing

We welcome contributions! Please create a pull request or open an issue for any suggestions or bug reports.

---

## License



