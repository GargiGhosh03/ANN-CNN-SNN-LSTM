
# 🧠 EEG Signal Classification with SNN, ANN, CNN, and LSTM

This project explores different neural network architectures for classifying EEG (electroencephalogram) brain signals, including:

- ⚡ **Spiking Neural Networks (SNN)** – biologically inspired neural models
- 🔧 **Artificial Neural Networks (ANN)** – simple fully connected layers
- 🌀 **Convolutional Neural Networks (CNN)** – spatial feature extractors
- 🔁 **Long Short-Term Memory (LSTM)** – temporal sequence models

---

## 📊 Objective

To evaluate and compare the effectiveness of biologically-inspired and deep learning models in classifying EEG signals from different cognitive or motor tasks.

---

## 🗃️ Dataset

- EEG data (e.g., [BCI Competition Dataset](http://www.bbci.de/competition/), DEAP, or synthetic EEG signals)
- Shape: `(samples, time_steps, channels)`
- Preprocessed to remove noise and artifacts.

---

## 🧠 Models Implemented

### 1. 🔁 LSTM
- Learns temporal dependencies in EEG sequences.
- Architecture: `LSTM → FC → Softmax`

### 2. 🌀 CNN
- Extracts spatial features across EEG channels.
- Architecture: `Conv1D/2D → ReLU → Pooling → FC → Softmax`

### 3. 🔧 ANN
- Baseline fully-connected architecture.
- Architecture: `FC → ReLU → FC → Softmax`

### 4. ⚡ SNN (Spiking Neural Network)
- Implemented using [`SpikingJelly`](https://github.com/fangwei123456/spikingjelly)
- Leaky Integrate-and-Fire (LIF) neurons
- Time-step based simulation with spike raster analysis

---

## 🧪 Evaluation Metrics

- ✅ Accuracy
- 📉 Loss curves
- 📊 Confusion Matrix
- ⚡ Raster Plots (for SNN)
- 🔥 Spike Rate Visualization

---

## 🧰 Requirements

```bash
pip install torch torchvision spikingjelly matplotlib numpy
```

---

## 🚀 Run

### 🔧 Train a Model
```bash
python train_ann.py
python train_cnn.py
python train_lstm.py
python train_snn.py
```

### 📈 Evaluate & Visualize
```bash
python evaluate.py
```

---

## 📂 Project Structure

```
📁 eeg-classification
│
├── data/                 # EEG data
├── models/               # ANN, CNN, LSTM, SNN definitions
├── train_ann.py
├── train_cnn.py
├── train_lstm.py
├── train_snn.py
├── utils/                # Preprocessing, loaders, plots
├── results/              # Plots, confusion matrices, spike data
└── README.md
```

---

## 🔬 Key Insights

- LSTM and CNN generally outperform ANN on temporal EEG data.
- SNNs produce comparable results and offer biologically plausible learning.
- Raster plots and spike rates reveal internal SNN activity.

---

## 📌 Future Work

- Add attention mechanism
- Fuse CNN + LSTM for hybrid models
- Apply to real-time EEG classification (e.g., BCI applications)

---

## 🧑‍💻 Author

Gargi Ghosh  
AI/ML Engineer | Neuroscience Enthusiast | Open Source Contributor
