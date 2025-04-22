## 📚 Self-Paced Learning with Knowledge Distillation for Improved Classification

This project implements a novel training pipeline that combines **Self-Paced Learning (SPL)** and **Knowledge Distillation (KD)** to improve classification performance by identifying and utilizing *easy* and *hard* samples during training.

## 🚀 Overview

Training deep learning models on noisy or complex datasets can lead to overfitting or poor generalization. This project addresses this challenge by:
1. Using **Self-Paced Learning** to identify *easy* and *hard* training samples dynamically.
2. Distilling knowledge from a **teacher model** trained on *easy samples* into a **student model** trained on both *easy and hard* samples.
3. Enhancing classification accuracy by combining curriculum learning principles with distillation.

---

## 🧠 Key Concepts

- **Self-Paced Learning (SPL):** A curriculum learning approach where the model is trained on *easier* samples first and gradually incorporates *harder* ones.
- **Knowledge Distillation (KD):** A method where a lightweight *student model* learns from a well-trained *teacher model*, capturing both output predictions and learned representations.
- **Easy vs. Hard Sample Classification:** Training samples are categorized based on model confidence or loss to create an adaptive training curriculum.

## 🔧 Installation

1. Clone the repo:
```bash
git clone https://github.com/your-username/self-paced-distillation-classifier.git
cd self-paced-distillation-classifier
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

---

## 🏗️ Training Pipeline

1. **Stage 1: Initial Training & Easy Sample Selection (SPL)**
   - Train a base classifier.
   - Compute loss or confidence scores for all samples.
   - Select *easy* samples based on threshold or ranking.

2. **Stage 2: Train Teacher Model on Easy Samples**
   - Fine-tune or train a teacher model using only easy samples.

3. **Stage 3: Train Student Model with KD on All Samples**
   - Train a student model using:
     - Ground-truth labels.
     - Teacher’s soft predictions for distillation.
     - Sample weights determined by SPL strategy.

---


## 📌 TODO

- [x] Implement SPL sample selector
- [x] Add distillation trainer
- [ ] Multi-teacher distillation
- [ ] Integrate with larger datasets (e.g., CIFAR-100, TinyImageNet)


## 📄 License

MIT License © 2025 Your Name

---

Let me know if you'd like to personalize this further or translate it into Persian.
