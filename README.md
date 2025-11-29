
# An Approach Based on Fine-Tuning Small Language Models for Fake News Detection

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-orange)](https://pytorch.org/)
[![Transformers](https://img.shields.io/badge/HuggingFace-Transformers-yellow)](https://huggingface.co/docs/transformers/index)
[![PEFT](https://img.shields.io/badge/PEFT-LoRA-green)](https://github.com/huggingface/peft)

**Authors:** [Khac-Lap Phan](mailto:lap4654100006@st.qnu.edu.vn)¹ and [Quang-Hung Le](mailto:lequanghung@qnu.edu.vn)²* **Affiliation:** Department of Information Technology, Quy Nhon University, Vietnam  
¹`lap4654100006@st.qnu.edu.vn`, ²`lequanghung@qnu.edu.vn` (Corresponding author)

---

## 📖 Abstract
The rapid proliferation of fake news on social media platforms poses
significant societal challenges. While Large Language Models (LLMs) achieve
high accuracy in detecting misinformation, their substantial computational costs
hinder deployment in resource-constrained environments. This study proposes a
lightweight approach utilizing Small Language Models (SLMs) to balance detection performance with efficiency. We implement a comparative pipeline utilizing
both Full Fine-Tuning and Low-Rank Adaptation (LoRA) to evaluate three SLM
architectures (DistilBERT, MiniLM, ALBERT) against a standard BERT-base
baseline across three diverse benchmarks: WELFake, LIAR, and FakeNewsNet.
Experimental results demonstrate that SLMs maintain remarkable robustness,
achieving 96–99% of the teacher model’s performance while reducing parameter counts by up to 90%. Notably, on the WELFake dataset, MiniLM achieves
an F1-score of 98.33% (within 0.4% of BERT-base) with a 3× increase in inference throughput. Furthermore, on the highly imbalanced FakeNewsNet dataset,
DistilBERT matches BERT-base’s F1-score (≈83.6%) while significantly lowering training loss. Our findings confirm that streamlined architectures, when coupled with parameter-efficient fine-tuning techniques, offer a scalable and highperformance solution for real-time fake news detection on edge devices.
## 🚀 Key Features
* **Small Language Models (SLMs):** Focused on efficient architectures:
    * DistilBERT
    * MiniLM
    * ALBERT
* **Fine-Tuning Strategies:**
    * Full Fine-Tuning
    * Parameter-Efficient Fine-Tuning (PEFT) using **LoRA** (Low-Rank Adaptation).
* **Comprehensive Evaluation:** Tested on WELFake, FakeNewsNet, and LIAR datasets.
* **High Efficiency:** Achieves comparable accuracy to BERT-base with significantly lower latency and computational cost.

## 📊 Performance Highlights

| Model | Method | Dataset | F1-Score | Inference Speed |
| :--- | :--- | :--- | :--- | :--- |
| **BERT-base** | Baseline | WELFake | ~98.7% | 1x |
| **MiniLM** | **LoRA** | **WELFake** | **98.33%** | **3x** |
| **DistilBERT** | Full FT | FakeNewsNet| ~83.6% | High |



