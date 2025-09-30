# 🧠 Deep Learning Project: Structured Latent Representations

This project explores learning structured latent representations from image data using three approaches:
1. Self-supervised Autoencoding
2. Classification-Guided Encoding
3. Contrastive Learning (SimCLR-inspired)

Each method was applied to both **MNIST** and **CIFAR-10** datasets.

---

## 📚 Methodology

### 1. Self-Supervised Autoencoding (`1.2.1`)
- **MNIST**: Fully connected autoencoder
- **CIFAR-10**: Convolutional autoencoder
- **Loss**: L1 (MAE)

### 2. Classification-Guided Encoding (`1.2.2`)
- Joint training of encoder and classifier
- Optimized for classification performance, not reconstruction
  
### 3. Contrastive Learning (`1.2.3`)
- SimCLR-style latent space learning using augmentations
- Encoder frozen, classifier trained on top

---

## 📊 Results

| Task   | Dataset  | Accuracy (Test) | Notes                         |
|--------|----------|-----------------|-------------------------------|
| 1.2.1  | MNIST    | 97.35%          | FC Autoencoder                |
|        | CIFAR-10 | 55.34%          | Conv AE, basic architecture   |
| 1.2.2  | MNIST    | 99.37%          | Classifier-guided FC          |
|        | CIFAR-10 | 82.27%          | CNN encoder + MLP classifier |
| 1.2.3  | MNIST    | 96.84%          | Contrastive (SimCLR-style)    |
|        | CIFAR-10 | 74.99%          | ResNet18 encoder              |

---

## 🧪 Datasets
- **MNIST**: 28×28 grayscale handwritten digits
- **CIFAR-10**: 32×32 RGB images from 10 natural image classes
---

## 🛠 Project Structure
```text
.
├── .idea/                 # IDE settings (can be ignored)
├── __pycache__/          # Python cache (can be ignored)
├── data/                 # Contains datasets
├── models/               # Saved models
├── results/              # Output JSON results per task
├── training/             # Scripts for training tasks
├── utils/                # Utility functions
├── _environment.yml      # Conda environment file
├── _main.py              # Entry-point script for training
├── _report_evaluation.py # Report generator
├── dry.pdf               # Theoretical Q&A answers
├── wet.pdf               # Full experiment report


## ⚙️ Usage

Install environment:
```bash
conda env create -f .environment.yml
conda activate <your_env>
```

Run training:
```bash
python _main.py --task 1.2.2 --dataset mnist
```

Evaluate:
```bash
python _report_evaluation.py
```
---

---

## ✍️ Author
This project was completed as part of a deep learning course assignment in 2025.
