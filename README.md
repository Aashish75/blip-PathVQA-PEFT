# blip-PathVQA-PEFT: Fine-Tuning BLIP on PathVQA with LoRA

This repository contains code for **fine-tuning the BLIP model** on the **PathVQA dataset** using **Parameter-Efficient Fine-Tuning (PEFT)** with **LoRA** (Low-Rank Adaptation). The goal is to optimize BLIP for **pathology-based Visual Question Answering (VQA)** while reducing computational overhead.

## 🚀 Project Overview
- Fine-tunes **[Salesforce/blip-vqa-base](https://huggingface.co/Salesforce/blip-vqa-base)** on the **PathVQA dataset**.
- Implements **LoRA (Low-Rank Adaptation)** instead of full fine-tuning to **reduce memory usage** while maintaining strong performance.
- Compares **LoRA fine-tuning vs. traditional full fine-tuning**.
- Evaluates model performance before and after fine-tuning.

---

## 📂 Dataset: PathVQA
- The dataset is loaded from the Hugging Face `datasets` library:
  ```python
  from datasets import load_dataset
  dataset = load_dataset("flaviagiammarino/path-vqa")

## 📊 Evaluation Results

The training significantly increased the capabilities of the base BLIP model in **pathological visual question answering (yes/no questions)**.

### **🔹 After LoRA Fine-Tuning**
| **Metric**  | **Score** |
|-------------|----------|
| Accuracy    | **85.19%** |
| Precision   | **85.89%** |
| Recall      | **86.84%** |
| F1 Score    | **86.36%** |

### **🔹 Before Fine-Tuning (BLIP Base Model)**
| **Metric**  | **Score** |
|-------------|----------|
| Accuracy    | **51.64%** |
| Precision   | **53.44%** |
| Recall      | **81.22%** |
| F1 Score    | **64.47%** |

### **🔹 Overall Improvements**
| **Metric**  | **Increase** |
|-------------|-------------|
| Accuracy    | **+33.55%** |
| Precision   | **+32.45%** |
| Recall      | **+5.62%** |
| F1 Score   

