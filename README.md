# Face Mask Detection using CNN  

*A deep learning project to classify images as "With Mask" or "Without Mask" using a Convolutional Neural Network (CNN).*  

---

## Introduction  
The COVID-19 pandemic highlighted the importance of mask compliance in public spaces.  
This project implements a **Convolutional Neural Network (CNN)** to automatically detect whether a person in an image is wearing a mask or not.  

---

## Dataset  
- **Source**: [Kaggle – Face Mask Dataset](https://www.kaggle.com/datasets/omkargurav/face-mask-dataset)  
- **Classes**:  
  - `With Mask` → labeled as 1  
  - `Without Mask` → labeled as 0  
- **Size**: Thousands of annotated face images in both categories.  

---

## Methodology  

### Data Preprocessing  
- Resized all images to **128×128 pixels**.  
- Normalized pixel values to [0,1].  
- Split dataset into **train / validation / test sets**.  

### CNN Architecture  
- **Conv2D + MaxPooling layers** for feature extraction.  
- **Dropout layers** to reduce overfitting.  
- **Dense output layer** with softmax activation (2 classes).  
- Optimizer: **Adam**  
- Loss: **Sparse Categorical Crossentropy**  

### Training  
- Epochs: 5 (configurable).  
- Validation split: 10%.  

---

## Results  

- **Test Accuracy**: ~ **94%**  
- **Classification Report**:  
  - *With Mask*: High precision & recall (>93%).  
  - *Without Mask*: High precision & recall (>94%).  
- Visualization: Plotted **training/validation accuracy** and **loss curves**.  
- Example prediction function created (`predict_mask`) to classify any input image with a confidence score.  

---

## Conclusion  

- The CNN achieved **robust performance (~94% accuracy)** in distinguishing between masked and unmasked faces.  
- Demonstrated how deep learning can support public health monitoring.  
- Future work:  
  - Increase dataset diversity (lighting, occlusions).  
  - Deploy model for **real-time detection** on edge devices.  

