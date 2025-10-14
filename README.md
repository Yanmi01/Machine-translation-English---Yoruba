# 🌍 Fine-tuning NLLB on Menyo-20k

This project fine-tunes **Meta’s NLLB (No Language Left Behind)** model using Parameter Efficient Fine-Tuning on the **Menyo-20k** dataset to improve translation quality for African languages. Training was conducted until early stopping to prevent overfitting.

---

## 📘 Overview

- **Model:** `facebook/nllb-200-distilled-600M`  
- **Dataset:** [Menyo-20k](https://github.com/bonaventuredossou/menyo-20k_mt) — parallel corpus for English–African language translation  
- **Goal:** Enhance NLLB performance on low-resource African languages (Yoruba, Igbo, Hausa, etc.)  
- **Framework:** Hugging Face Transformers  

---

## ⚙️ Training Setup

| Setting | Value |
|----------|--------|
| Batch Size | 8 |
| Learning Rate | 1e-4 |
| Gradient Accumulation Step| 8 |
| Scheduler | Cosine |
| Epochs | 50 |
| Early Stopping | Patience = 10 |
| Environment | Kaggle (T4 GPU x 2) |

---

## 🧩 Method

1. Preprocess and tokenize Menyo-20k using NLLB tokenizer  
2. Fine-tune the model using LoRA and with Huggingface Trainer 
3. Apply early stopping based on validation loss  
4. Evaluate with BLEU and qualitative translation tests  

---




