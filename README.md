# 🌐 Multilingual Neural Machine Translation (100+ Languages)

A production-level multilingual Neural Machine Translation system using **facebook/m2m100_418M** (418M parameters), supporting translation across 100+ languages with dual-metric evaluation — BLEU Score and Semantic Similarity.

---

## 🎯 Demo

```
===== AI Translator Menu =====
1. Translate Text
2. Exit

Enter text: The rapid advancement of technology has transformed the way people communicate.
Enter target language (fr/de/hi/es/en): de

Translated Output: Die rasante Entwicklung der Technologie hat die Art und Weise verändert...
Translation Time: 2.847 seconds

Do you want evaluation? (yes/no): yes
Enter reference translation: ...
Choose evaluation method:
1. BLEU Score
2. Embedding Similarity
3. Both

BLEU Score: 0.6842
Embedding Similarity: 0.9134
```

---

## ⚙️ Tech Stack

| Component | Tool |
|-----------|------|
| Translation Model | `facebook/m2m100_418M` (418M params, 100+ languages) |
| Tokenizer | `M2M100Tokenizer` (Hugging Face) |
| Semantic Evaluation | `all-MiniLM-L6-v2` (SentenceTransformer) |
| BLEU Evaluation | `nltk.translate.bleu_score` |
| Language Detection | `langdetect` |
| Similarity Metric | Cosine Similarity (sklearn) |
| Framework | PyTorch + Hugging Face Transformers |
| Environment | Google Colab (GPU) |

---

## 🌍 Supported Languages

| Code | Language |
|------|----------|
| `en` | English |
| `fr` | French |
| `de` | German |
| `hi` | Hindi |
| `es` | Spanish |
| `zh` | Chinese |
| `ar` | Arabic |

> Model supports 100+ languages total via M2M100 architecture.

---

## 📁 Project Structure

```
multilingual-nmt/
│
├── Machine_Translation_Final.ipynb   # Main Colab notebook
├── requirements.txt
└── README.md
```

---

## 🔧 Setup & Run

### 1. Clone the repo
```bash
git clone https://github.com/chhaviawasthi-svg/multilingual-nmt.git
cd multilingual-nmt
```

### 2. Install dependencies
```bash
pip install transformers sentencepiece langdetect nltk sentence-transformers scikit-learn
```

### 3. Run on Google Colab (Recommended)
- Open `Machine_Translation_Final.ipynb` in Colab
- Set Runtime → **GPU (T4 or better)** — model is 418M params
- Run all cells

---

## 📊 Evaluation — Dual Metric System

This project evaluates translation quality using **two complementary metrics:**

| Metric | Method | What it measures |
|--------|--------|-----------------|
| BLEU Score | `nltk.translate.bleu_score` | n-gram overlap with reference |
| Embedding Similarity | Cosine via `all-MiniLM-L6-v2` | Semantic meaning preservation |

> BLEU alone misses paraphrase quality — combining with embedding similarity gives a more complete picture of translation accuracy.

---

## 🔑 Key Features

- ✅ `facebook/m2m100_418M` — 418M parameter multilingual model (100+ languages)
- ✅ Paragraph-level translation with sentence segmentation
- ✅ Dual evaluation: BLEU Score + Semantic Similarity (cosine)
- ✅ Interactive CLI menu for real-time translation & evaluation
- ✅ Execution time measurement per translation
- ✅ Hindi language support — relevant for Indian NLP applications
- ✅ Language detection via `langdetect`

---

## 🔮 Future Improvements

- [ ] Fine-tune M2M100 on domain-specific corpus (medical / legal)
- [ ] Add FastAPI / Gradio web interface for live demo
- [ ] Extend evaluation with METEOR and chrF scores
- [ ] Batch translation support for large documents

---

## 👩‍💻 Author

**Chhavi Awasthi**
M.Tech — Mathematics & Computing, IIT (ISM) Dhanbad
CSIR NET AIR 35 | GATE Mathematics AIR 197

[![LinkedIn](https://img.shields.io/badge/LinkedIn-chhaviawasthi-blue)](https://linkedin.com/in/chhaviawasthi)
[![GitHub](https://img.shields.io/badge/GitHub-chhaviawasthi--svg-black)](https://github.com/chhaviawasthi-svg)
