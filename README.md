
# An Approach Based on Fine-Tuning Small Language Models for Fake News Detection

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-orange)](https://pytorch.org/)
[![Transformers](https://img.shields.io/badge/HuggingFace-Transformers-yellow)](https://huggingface.co/docs/transformers/index)
[![PEFT](https://img.shields.io/badge/PEFT-LoRA-green)](https://github.com/huggingface/peft)

---

## Abstract
The rapid proliferation of fake news on social media platforms poses significant societal challenges. While Large Language Models (LLMs) achieve high accuracy in detecting misinformation, their substantial computational costs hinder deployment in resource-constrained environments. This study proposes a lightweight approach utilizing Small Language Models (SLMs) to balance detection performance with efficiency. We implement a comparative pipeline utilizing both Full Fine-Tuning and Low-Rank Adaptation (LoRA) to evaluate three SLM architectures (DistilBERT, MiniLM, ALBERT) against a standard BERT-base baseline across three diverse benchmarks: WELFake, LIAR, and FakeNewsNet.Experimental results demonstrate that SLMs maintain remarkable robustness, achieving 96–99% of the teacher model’s performance while reducing parameter counts by up to 90%. Notably, on the WELFake dataset, MiniLM achieves an F1-score of 98.33% (within 0.4% of BERT-base) with a 3× increase in inference throughput. Furthermore, on the highly imbalanced FakeNewsNet dataset, DistilBERT matches BERT-base’s F1-score (≈83.6%) while significantly lowering training loss. Our findings confirm that streamlined architectures, when coupled with parameter-efficient fine-tuning techniques, offer a scalable and high-performance solution for real-time fake news detection on edge devices.

## Citation
If you use this code or our results in your research, please cite our paper:

```bibtex
@article{Phan2025SLMFakeNews,
  title={An Approach Based on Fine-Tuning Small Language Models for Fake News Detection},
  author={Phan, Khac-Lap and Le, Quang-Hung},
  journal={Department of Information Technology, Quy Nhon University},
  year={2025}
}

