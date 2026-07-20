# UgvNet01
----
# UgvNet01: Deep Learning Model for Multi-Class Skin Disease Detection

[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)](https://pytorch.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Accuracy](https://img.shields.io/badge/Validation_Accuracy-99.59%25-brightgreen?style=for-the-badge)](https://github.com/Onik-Howlader/UgvNet01)
---
**UgvNet01** is an optimized, lightweight Convolutional Neural Network (CNN) architecture designed for automated, high-precision dermatological disease classification. It achieves a **99.59% validation accuracy** across 6 distinct skin condition categories.

---

## 📌 Key Features
- **High Accuracy:** 99.59% overall accuracy with a low loss of `0.0225`.
- **Supported Classes (6):** 
  - Atopic Dermatitis (AD)
  - Contact Dermatitis (CD)
  - Eczema (EC)
  - Scabies (SC)
  - Seborrheic Dermatitis (SD)
  - Tinea Corporis (TC)
- **Efficient & Lightweight:** Designed for fast inference and deployment in edge-AI / tele-dermatology systems.

---

## 📊 Benchmark Results

| Metric | Score |
| :--- | :---: |
| **Validation Accuracy** | **99.59%** |
| **Validation Loss** | **0.0225** |
| **Macro F1-Score** | **0.9961** |
| **Macro Precision** | **0.9953** |
| **Macro Recall** | **0.9970** |

---

## 💻 How to Use

### 1. Clone the Repository
```bash
git clone [https://github.com/Onik-Howlader/UgvNet01.git](https://github.com/Onik-Howlader/UgvNet01.git)
cd UgvNet01

### 2. Load the Pretrained Model via Hugging Face Hub

```python
import torch
from huggingface_hub import hf_hub_download

# Download weights from Hugging Face Hub
model_path = hf_hub_download(
    repo_id="Onik-Howlader/UgvNet01", 
    filename="UgvNet01_best_model.pth"
)

# Initialize and load model weights
model = UgvNet01(num_classes=6)
model.load_state_dict(torch.load(model_path))
model.eval()

print(" UgvNet01 Model Loaded Successfully!")
3. Repository Structure
├── UgvNet01.ipynb           # Training & Evaluation Notebook
├── README.md                # Project Documentation
└── LICENSE                  # MIT License
4. Citation & License
  Distributed under the MIT License. See LICENSE for more information.
  If you use UgvNet01 in your research, please consider citing this project.
