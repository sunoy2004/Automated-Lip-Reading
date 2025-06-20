# 👄 Automated Lip Reading Using CNN, LSTM, GRU & TCN

An end-to-end deep learning system that interprets **silent lip movements** and transcribes them into text using cutting-edge models like CNN+LSTM and CNN+GRU. Built for assistive tech, silent communication, and real-time visual speech recognition.

---

## 🧠 Project Summary

**LipNet**, the foundation of this project, is a breakthrough in visual speech recognition. It transcribes entire sentences directly from sequences of lip movements, without needing audio input or phoneme-level annotations.

We explore multiple configurations using:

* CNN + GRU
* CNN + Bi-LSTM
* 3D CNN + Temporal Convolutional Networks (TCNs)

---

## 🎯 Objectives

* Decode speech purely from visual lip motion.
* Enable communication in noisy environments or for the hearing-impaired.
* Provide a real-time, scalable lip-reading pipeline using deep learning.

---

## 📁 Dataset

We use the **GRID Corpus**, a standard benchmark dataset in visual speech recognition:

```
/data/
  ├── s1/
  │   └── bbaf2n.mpg  # Video samples
  └── alignments/s1/
      └── bbaf2n.align  # Character-level transcriptions
```

---

## ⚙️ Pipeline Overview

1. **Frame Extraction** (OpenCV)
2. **Lip Region Detection** (Facial landmarks)
3. **Grayscale Conversion & Resizing**
4. **Sequence Modeling** using RNNs (GRU/LSTM)
5. **CTC Loss** for training without frame-level alignment
6. **Text Decoding** (Greedy / Beam Search)

---

## 🏗️ Model Configurations

| Model       | Architecture         | Epochs | Accuracy  | Training Time |
| ----------- | -------------------- | ------ | --------- | ------------- |
| **Model 1** | CNN + GRU            | 10     | 91%       | Fast          |
| **Model 2** | CNN + LSTM (deep)    | 100    | **95.4%** | \~12 hours    |
| **Model 3** | CNN + GRU (extended) | 100    | 92%       | \~7 hours     |
| **Model 4** | 3D CNN + TCN         | 9      | 82.7%     | **5 mins**    |

---

## 🧪 Results

* **Character Error Rate (CER):** \~4.8%
* **Word Error Rate (WER):** \~11.4% on unseen speakers
* **Robust generalization** across lighting, faces, and speaking styles

> *“How are you doing today?” ← Predicted accurately from silent lip motion!*

---

## 🧰 Technologies Used

* 🧠 **TensorFlow / PyTorch**
* 📦 **OpenCV, NumPy, Sci-Kit Learn**
* 🗂️ GRID Corpus
* 🧪 **CTC Loss**
* 🌀 GRUs, LSTMs, TCNs
* 🎛️ Colab-based notebooks

---

## 🧪 Evaluation Metrics

* ✔️ Word Error Rate (WER)
* ✔️ Character Error Rate (CER)
* ✔️ Validation Accuracy
* 🔍 Saliency Maps for interpretability

---

## 🚀 Future Scope

* Real-world, multilingual datasets (e.g., LRS3)
* Transformer & TCN-based architectures
* Multimodal integration (audio + visual)
* Deployment in assistive technologies & mobile apps
* Explainable AI (XAI) visualizations for trust

---

## 📚 References

* [LipNet: Assael et al. (2016)](https://arxiv.org/abs/1611.01599)
* [WAS: Chung et al. (2017)](https://ieeexplore.ieee.org/document/8063416)
* [GRID Corpus Overview](http://spandh.dcs.shef.ac.uk/gridcorpus/)
* See full [research paper](./LipReading_Research.pdf) for detailed methodology and citations.

---

## 👨‍🏫 Team

* **Sunoy Roy (UI22CS77)**
* Aman Khan (UI22CS05)
* Prashasti Vyas (UI22CS61)
* Supervisor: **Dr. Ritesh Kumar**, IIIT Surat

---

## 📂 Repository Structure

```bash
📁 data/
📁 models/
├── cnn_gru.ipynb
├── cnn_lstm.ipynb
├── 3dcnn_tcn.ipynb
📄 LipReading_Research.pdf
📄 MiniProject_Presentation.pdf
📄 README.md
```

---

## 🌟 Highlights

* ⚡ Real-time inference with GRU-based model
* 🎯 Highest accuracy with deep LSTM model
* 🧠 No handcrafted features or audio needed
* 💬 Future-ready for assistive speech technologies

---

