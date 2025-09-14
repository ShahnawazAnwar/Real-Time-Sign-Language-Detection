# Real-Time Sign Language Detection Using Human Pose Estimation

## Presented by: Shahnawaz Anwar

---

##  Project Overview

**Objective:**  
To facilitate communication for the deaf community by developing a real-time sign language detection system.

**Methodology:**  
This project leverages a simplified human optical-flow encoding for videos based on pose estimation.

**Dataset:**  
- **[WLASL](https://github.com/dxli94/WLASL):** The Word-Level American Sign Language dataset, containing over 12,000 videos—currently the largest of its kind.

---

## 🛠 Technical Skills & Technologies

### Technical Skills

- **Deep Learning:** Model development for sign language detection.
- **Computer Vision:** Human pose estimation, optical flow, and landmark extraction.
- **Data Pre-processing:** Video data preparation and manipulation.
- **Model Training & Evaluation:** Handling imbalanced datasets (oversampling), using performance metrics.
- **Python Programming:** Leveraging popular ML and CV libraries.

### Technologies Used

- **Media Pipe Holistic:** Pre-trained model for extracting landmark keypoints from video frames.
- **Keras:** Deep learning API for model building.
- **LSTM:** Long Short-Term Memory networks for temporal data processing.
- **Adam Optimizer:** Optimization algorithm used during training.

---

## Methodology & Working Algorithm

1. **Human Pose Estimation (HPE):**  
   - Identifies and distinguishes a person's joints to create a skeleton-like representation.

2. **Data Pre-processing:**  
   - Each video is processed to extract 30 frames.
   - [MediaPipe Holistic](https://google.github.io/mediapipe/) extracts **1,662 landmark keypoints per frame**:
     - 33 body pose
     - 468 face
     - 21 per hand

3. **Model Preparation:**  
   - Data is **spatiotemporal** (both spatial and temporal features).
   - Utilizes an LSTM model with dense layers for sequence modeling.

4. **Model Training:**  
   - Trained on 90% of the dataset using Adam optimizer.
   - Oversampling techniques used to handle dataset imbalance.

5. **Model Evaluation:**  
   - Metrics: **Accuracy**, **Loss**, and **Confusion Matrix**.

---

##  Key Results

- **Training & Validation Accuracy:** Both plateaued at approximately **60%**.
- **Test Accuracy:** Achieved **63%** on 11 randomly selected videos.
- **Performance Metrics:** Precision, recall, and F1-score were each **63%**.

---

## Conclusion & Future Work

- The project establishes a strong foundation for **word-level sign language recognition** using the WLASL dataset.
- **Future Plans:**
  - Scale the algorithm to classify all 2,000 classes from the dataset.
  - Enhance performance using more powerful computational resources.
  - Explore real-time deployment and integration with assistive technologies.

- [MediaPipe Holistic](https://google.github.io/mediapipe/solutions/holistic.html)

