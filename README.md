# 🧠 Optimizing a Character-Level Transformer LLM in PyTorch

This project focuses on improving the training performance and generation quality of a character-level Transformer-based language model trained on Shakespearean text. The model was optimized across architecture, data processing, training configuration, regularization, and sampling — all without increasing the number of training steps.

---

## 🔧 Optimization Overview

### 📐 Model Architecture
- Increased the number of Transformer blocks (layers) and multi-head attention heads
- Expanded embedding and feed-forward dimensions to enhance token representation

### 🧹 Data Processing
- Cleaned dataset by removing invalid and non-ASCII characters
- Standardized sequence formatting to ensure consistent batch processing

### ⚙️ Training Configuration
- Switched to the AdamW optimizer for improved weight decay control
- Applied OneCycleLR scheduler to dynamically adjust the learning rate throughout training
- Enabled gradient clipping to improve stability during backpropagation

### 🛡️ Regularization Strategy
- Introduced dropout within Transformer blocks to reduce overfitting
- Balanced regularization to maintain convergence speed and generalization

### 🎯 Sampling and Generation
- Fine-tuned generation output using temperature scaling, top-k sampling, and nucleus (top-p) sampling
- Used structured prompts to evaluate and refine output diversity and coherence

---

## 📈 Summary

This project demonstrates how strategic modifications to model design and training strategy can significantly improve the performance of a lightweight Transformer LLM. The model became more stable during training and produced more coherent and stylistically appropriate text, all while operating under the same training step constraints as the original baseline.
