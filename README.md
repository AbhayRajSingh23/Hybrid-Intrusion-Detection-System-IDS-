# 🛡️ Hybrid Intrusion Detection System (IDS)

A Machine Learning + Deep Learning based Hybrid Intrusion Detection System built using the NSL-KDD dataset.

This project combines:

- 🔎 Signature-Based Detection (Regex Rules)
- 🌳 Misuse Detection (Random Forest)
- 🧠 Anomaly Detection (Autoencoder)

---

## 📖 Project Overview

Traditional IDS systems struggle to detect zero-day attacks while maintaining high accuracy for known attacks.

This Hybrid IDS solves that by combining:

1. Rule-based signature detection for known payload attacks
2. Supervised learning (Random Forest) for known attack patterns
3. Unsupervised anomaly detection (Autoencoder) for novel attacks

---

## 📊 Dataset

- **NSL-KDD Dataset**
- Binary classification: `normal` vs `attack`
- 122 engineered features after encoding

---

## ⚙️ System Architecture

Signature Check ➜ Random Forest ➜ Autoencoder

If any stage detects an attack, traffic is flagged.

---

## 🧠 Models Used

### 🌳 Random Forest (Misuse Detection)
- 100 estimators
- Max depth: 10
- Detects known attack patterns
- Evaluated using:
  - Confusion Matrix
  - ROC Curve
  - Classification Report

### 🧠 Autoencoder (Anomaly Detection)
- Trained ONLY on normal traffic
- Bottleneck architecture (32 → 16 → 32)
- Threshold = Mean + 3 × Std Dev (Reconstruction Error)
- Detects zero-day / unseen attacks

---

## 📈 Results

| Model | Purpose | Strength |
|-------|--------|----------|
| Signature | Fast rule detection | Known payload attacks |
| Random Forest | Supervised learning | Known feature patterns |
| Autoencoder | Unsupervised | Novel / zero-day attacks |

The hybrid system improves detection robustness while reducing false negatives.

---

## 🛠️ Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn
- TensorFlow / Keras
- Matplotlib / Seaborn

---

## ▶️ How to Run

### 1️⃣ Clone the repository

```bash
git clone https://github.com/your-username/Hybrid-Intrusion-Detection-System.git
cd Hybrid-Intrusion-Detection-System
````

### 2️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Run the script

```bash
python src/hybrid_ids.py
```

Or open the notebook inside `/notebooks`.

---

## 🔐 Hybrid Decision Flow

1. Check payload against attack signatures
2. If not detected → Random Forest classification
3. If still safe → Autoencoder anomaly detection
4. Final decision returned

---

## 🚀 Future Improvements

* Multi-class attack classification
* Real-time packet capture integration (Scapy)
* REST API deployment (FastAPI)
* Docker containerization
* SIEM integration

---

## 👨‍💻 Author

Abhay Raj Singh
B.Tech Information Technology
Business Analytics Minor
HBTU Kanpur

GitHub: [https://github.com/AbhayRajSingh23](https://github.com/AbhayRajSingh23)
```

---

# 🎯 Make This Resume-Ready (VERY IMPORTANT)

Add this to your resume:

### Hybrid Intrusion Detection System (ML + DL)
- Designed and implemented a hybrid IDS combining signature-based rules, Random Forest classifier, and Autoencoder anomaly detection.
- Achieved robust detection of both known and zero-day attacks using NSL-KDD dataset.
- Implemented One-Hot Encoding and feature scaling for 122 engineered features.
- Evaluated models using ROC curves, confusion matrices, and reconstruction error thresholds.

---

# 💎 If You Want to Make It EVEN STRONGER

Since you're targeting backend/full-stack roles, improve it by:

### 🔥 1. Convert it to an API
Use FastAPI:


POST /predict


### 🔥 2. Dockerize It
Add Dockerfile → recruiters love that.

### 🔥 3. Add Model Saving
Save RF and AE models using:


joblib
model.save()



---

# 🧠 Honest Opinion (Mentor Mode)

Abhay, this project is:

✔ Better than typical college ML projects  
✔ Interview-discussable  
✔ Strong for cybersecurity + AI roles  
✔ Shows supervised + unsupervised understanding  
✔ Shows system design thinking  

If polished properly, this can become your **best resume project**.

---

If you want, next I can:

- 🔥 Help you convert this into a REST API
- 🔥 Help you Dockerize it
- 🔥 Help you write interview answers for this project
- 🔥 Help you deploy it on Render / Railway

Tell me what you want next.
```
