# 🌐 AI-Based Neural Machine Translation (Seq2Seq Transformer)

A Transformer-based Neural Machine Translation system built **from scratch** using PyTorch, implementing the full encoder-decoder architecture for multilingual text translation.

---

## 🚀 Demo

```
Input  (English): "The model learns from data."
Output (French) : "Le modèle apprend des données."
```

---

## 🧠 Architecture

```
Input Tokens
     ↓
[Embedding + Positional Encoding]
     ↓
[Encoder Stack]
  └── Multi-Head Self-Attention
  └── Feed Forward Network
  └── Layer Normalization
     ↓
[Decoder Stack]
  └── Masked Multi-Head Self-Attention
  └── Cross-Attention (Encoder-Decoder)
  └── Feed Forward Network
     ↓
[Linear + Softmax]
     ↓
Output Tokens
```

---

## ⚙️ Tech Stack

| Component | Tool |
|-----------|------|
| Framework | PyTorch |
| Pretrained Models & Tokenizers | Hugging Face Transformers |
| Models Used | mBART, Helsinki-NLP |
| GPU Acceleration | CUDA |
| Evaluation Metric | BLEU Score |
| Environment | Google Colab / PyCharm |

---

## 📁 Project Structure

```
neural-machine-translation/
│
├── nmt_transformer.ipynb       # Main notebook (Colab)
├── model/
│   ├── encoder.py              # Encoder stack
│   ├── decoder.py              # Decoder stack
│   ├── attention.py            # Multi-head attention
│   └── transformer.py          # Full model
├── utils/
│   ├── tokenizer.py            # Hugging Face tokenizer wrapper
│   └── bleu.py                 # BLEU score evaluation
├── requirements.txt
└── README.md
```

---

## 🔧 Setup & Run

### 1. Clone the repo
```bash
git clone https://github.com/chhaviawasthi-svg/neural-machine-translation.git
cd neural-machine-translation
```

### 2. Install dependencies
```bash
pip install torch transformers datasets sacrebleu
```

### 3. Run on Google Colab (Recommended)
- Open `nmt_transformer.ipynb` in Google Colab
- Set Runtime → **GPU (T4 or better)**
- Run all cells

### 4. Run locally
```bash
python model/transformer.py
```

---

## 📊 Results

| Training Setup | Epoch Time | BLEU Score |
|----------------|------------|------------|
| CPU only | ~45 min/epoch | baseline |
| CUDA GPU | ~18 min/epoch | improved |
| + Hugging Face tokenizers | ~18 min/epoch | best |

> CUDA-accelerated training reduced epoch time by **~60%** compared to CPU baseline.

---

## 🔑 Key Concepts Implemented

- ✅ Multi-head self-attention from scratch
- ✅ Positional encoding
- ✅ Encoder-decoder architecture
- ✅ Masked attention in decoder
- ✅ Hugging Face multilingual tokenizers (mBART / Helsinki-NLP)
- ✅ BLEU score evaluation
- ✅ CUDA-accelerated training

---

## 👩‍💻 Author

**Chhavi Awasthi**
M.Tech — Mathematics & Computing, IIT (ISM) Dhanbad
CSIR NET AIR 35 | GATE Mathematics AIR 197

[![LinkedIn](https://img.shields.io/badge/LinkedIn-chhaviawasthi-blue)](https://linkedin.com/in/chhaviawasthi)
[![GitHub](https://img.shields.io/badge/GitHub-chhaviawasthi--svg-black)](https://github.com/chhaviawasthi-svg)
