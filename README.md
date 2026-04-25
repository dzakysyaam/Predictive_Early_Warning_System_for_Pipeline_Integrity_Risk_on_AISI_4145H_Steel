# PETRUG  
AI-Based Predictive Early Warning System for Pipeline Integrity Risk  
on AISI 4145H Steel Using Pressure and Flow Dynamics

---

## 📌 Deskripsi Proyek

PETRUG merupakan Proof of Concept (PoC) sistem berbasis Machine Learning yang dirancang untuk mendeteksi dan memprediksi risiko integritas pipeline secara dini pada operasi hulu minyak dan gas. Sistem ini memanfaatkan parameter operasional seperti tekanan, laju aliran, dan dinamika perubahan kondisi untuk mengidentifikasi potensi risiko sebelum berkembang menjadi gangguan yang lebih serius.

Pendekatan yang digunakan tidak bergantung pada penambahan sensor baru, melainkan memanfaatkan data operasional yang sudah tersedia, sehingga lebih efisien dan mudah diadopsi.

---

## 🎯 Tujuan

- Mengembangkan sistem peringatan dini berbasis AI untuk risiko pipeline  
- Mengidentifikasi pola kondisi Normal, Warning, dan Critical  
- Mendukung pengambilan keputusan operasional secara lebih cepat dan terstruktur  
- Mengurangi potensi kehilangan produksi akibat keterlambatan deteksi  

---

## 🧠 Metodologi

Pengembangan sistem menggunakan pendekatan **CRISP-DM**:

1. Business Understanding  
2. Data Understanding  
3. Data Preparation  
4. Modeling  
5. Evaluation  
6. Deployment (PoC)

---

## 📊 Dataset

Dataset yang digunakan bersifat **synthetic SCADA-based dataset** dengan parameter utama:

- Pressure (MPa)  
- Flow Rate (m3/h)  
- Flow Velocity (m/s)  
- Temperature (°C)  
- dP/dt (perubahan tekanan)  
- dT/dt (perubahan suhu)  
- Acoustic Emission  
- Strain  

Target output:
- Normal  
- Warning  
- Critical  

---

## ⚙️ Feature Engineering

Beberapa fitur tambahan yang digunakan:

- Pressure_Flow_Ratio  
- Temperature_Pressure_Index  
- Pressure_Change_Abs  
- Temperature_Change_Abs  

Fitur dipilih untuk tetap relevan dengan konteks **pressure dan flow dynamics** sesuai fokus penelitian.

---

## 🤖 Model Machine Learning

Model yang digunakan:

- Gradient Boosting  
- Random Forest  
- Logistic Regression  
- Support Vector Machine  
- K-Nearest Neighbour  
- Decision Tree  

Model terbaik:
- **Random Forest**

---

## 📈 Hasil Evaluasi

Model terbaik (Random Forest) menunjukkan performa sebagai berikut:

- Accuracy: 0.975  
- F1-score (weighted): 0.9753  

Performa per kelas:
- Normal: F1-score 0.98  
- Warning: F1-score 0.94  
- Critical: F1-score 1.00  

Evaluasi dilakukan menggunakan:
- Confusion Matrix  
- Accuracy  
- Precision  
- Recall  
- F1-score  
- Cross-validation  

---

## ⚠️ Catatan Evaluasi

Dataset pada tahap Proof of Concept masih bersifat sintetis, sehingga beberapa pola antar kelas relatif lebih terpisah dibandingkan kondisi nyata. Untuk menjaga validitas model, dilakukan pembatasan fitur dan regularisasi agar model tetap generalizable dan tidak overfitting.

---

## 🚀 Inference (Simulasi)

Model dapat digunakan untuk memprediksi kondisi pipeline secara langsung berdasarkan input data operasional, seperti:

- Pressure  
- Flow Rate  
- Temperature  
- Perubahan tekanan dan suhu  

Output:
- Prediksi status risiko (Normal / Warning / Critical)  
- Confidence level  

---

## 💻 Teknologi yang Digunakan

- Python  
- Google Colab  
- Visual Studio Code  
- Pandas & NumPy  
- Scikit-learn  
- Plotly  
- Statsmodels  
- Streamlit  

---

## 💰 Efisiensi Biaya

Solusi ini dirancang dengan pendekatan cost-efficient:

- Software: berbasis open-source  
- Infrastruktur: minimal (PoC)  
- Tidak memerlukan sensor tambahan  

Sehingga mudah diimplementasikan dan dikembangkan lebih lanjut.

---

## 📌 Kesimpulan

PETRUG menunjukkan bahwa pendekatan berbasis Machine Learning dapat digunakan sebagai alat bantu untuk mendeteksi risiko pipeline secara lebih dini. Dengan memanfaatkan data operasional yang tersedia, sistem ini berpotensi meningkatkan keandalan fasilitas, mengurangi risiko gangguan operasional, serta mendukung strategi maintenance yang lebih proaktif.

---

## 👨‍💻 Pengembangan Selanjutnya

- Integrasi dengan sistem SCADA real-time  
- Deployment ke dashboard monitoring industri  
- Penambahan data real untuk validasi lebih lanjut  
- Pengembangan model prediksi RUL  

---
