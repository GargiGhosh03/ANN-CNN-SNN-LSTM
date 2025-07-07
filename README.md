# ANN-CNN-SNN-LSTM
Implementation of CNN, ANN, LSTM and SNN on the EEG Brainwave dataset

🗃️ Dataset
EEG data (e.g., BCI Competition Dataset, DEAP, or synthetic EEG signals)

Shape: (samples, time_steps, channels)

Preprocessed to remove noise and artifacts.

🧠 Models Implemented
1. 🔁 LSTM
Learns temporal dependencies in EEG sequences.

Architecture: LSTM → FC → Softmax

2. 🌀 CNN
Extracts spatial features across EEG channels.

Architecture: Conv1D/2D → ReLU → Pooling → FC → Softmax

3. 🔧 ANN
Baseline fully-connected architecture.

Architecture: FC → ReLU → FC → Softmax

4. ⚡ SNN (Spiking Neural Network)
Implemented using SpikingJelly

Leaky Integrate-and-Fire (LIF) neurons

Time-step based simulation with spike raster analysis

