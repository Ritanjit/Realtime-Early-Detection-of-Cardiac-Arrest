# 🫀 Early Detection of Cardiac Arrest using Deep Learning

This project presents a deep learning-based early detection system for cardiac arrest using ECG signals. Leveraging a 1D Convolutional Neural Network (CNN), the system analyzes real-time biometric data to detect critical arrhythmias that may lead to sudden cardiac arrest.

[![Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1uRpSNWPYPE__Nhhtnl6-anwPlyJU5OGz#scrollTo=vWpy8lJWN45l)

---

## 📌 Objective

To build an efficient and lightweight model for early detection of life-threatening cardiac conditions using ECG signals. The system should be capable of processing and interpreting streaming biomedical signals in real-time.

---

## 🧠 Model Architecture

- **Type:** 1D Convolutional Neural Network (CNN)
- **Layers:**  
  - 5 Convolution + Average Pooling blocks  
  - 1 Dropout layer  
  - 2 Fully Connected layers  
  - Softmax output (5-class classification)
- **Input:** 360-sample ECG beat window
- **Output Classes:**  
  - `N` (Normal)  
  - `L` (Left bundle branch block)  
  - `R` (Right bundle branch block)  
  - `A` (Atrial premature)  
  - `V` (Ventricular premature)

---

## 📊 Dataset

- **Source:** [MIT-BIH Arrhythmia Database](https://www.physionet.org/content/mitdb/1.0.0/)
- **Format:** `.csv` (ECG signals) and `.txt` (annotations)
- **Preprocessing:**
  - Discrete Wavelet Transform (Symlet-4) for denoising
  - Z-score normalization
  - Windowing around R-peaks

---

## 🚀 Getting Started

### 🔧 Requirements
- Python 3.x
- TensorFlow / Keras
- Pandas, NumPy, PyWavelets, Matplotlib

### 🧪 How to Use

1. **Clone this repo:**
   ```bash
   git clone https://github.com/Ritanjit/early-detection-cardiac-arrest.git
   cd early-detection-cardiac-arrest
   
2. **Run in Google Colab:**
   
  &nbsp;&nbsp; Click the badge below to open directly in Colab:

  &nbsp;&nbsp; [![Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1uRpSNWPYPE__Nhhtnl6-anwPlyJU5OGz#scrollTo=vWpy8lJWN45l)

---

### Model Workflow:

1. **Load ECG signal**

2. **Preprocess and extract beat windows**

3. **Run real-time inference via a sliding window**

4. **Detect and alert on dangerous rhythms**

---

### 🎯 Output & Results

📈 **Model Accuracy: ~96% on test set**

🟢 **Real-time alerts for ventricular arrhythmia with probability > 0.8**

📉 **Class balancing via upsampling/downsampling**

📊 **Pie charts for class distribution pre/post-balancing**

---

###  📈 Future Work

1. **Integrate lightweight models like ResNet1D or MobileNet1D**

2. **Deploy as a mobile/web app for remote monitoring**

3. **Extend to multi-lead ECG and multi-modal biosignals**

4. **Add hardware support for real-time streaming (Raspberry Pi + ECG module)**

---

### 📬 Contact
**For questions or collaboration:**
**Ritanjit Das**
**ritanjitdas.dev@gmail.com**

---


