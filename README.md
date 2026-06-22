# 🚨 Real-Time Anomaly Detection

Streaming-style anomaly detection with Isolation Forest, simulating how outliers are flagged as data arrives over time.

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-IsolationForest-orange.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626.svg)

**🌐 Language:** English · [Türkçe](#-türkçe)

## ⚡ Overview

Anomaly detection matters wherever rare events signal trouble — fraud, equipment faults, network intrusions. This project trains an **Isolation Forest** and then replays the data as a live stream, scoring each incoming point and updating the visualization in real time.

## 📊 Dataset

A tabular dataset of numeric features (loaded from Google Drive in Colab); each row is treated as one "tick" of an incoming data stream.

## 🧠 Approach

1. **Preprocessing** — load the data, standardize features with `StandardScaler`.
2. **Model** — fit an **Isolation Forest**, an unsupervised algorithm that isolates outliers using random partitioning.
3. **Real-time simulation** — iterate through the data with a timing loop, scoring points one by one and refreshing a live plot (`clear_output`) to mimic a monitoring dashboard.
4. **Evaluation** — summarize results with a `classification_report` and `confusion_matrix`.

## 🛠️ Tech Stack

`Python` · `pandas` · `numpy` · `scikit-learn` (IsolationForest, StandardScaler) · `matplotlib` · `seaborn`

## ▶️ How to Run

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
jupyter notebook RealTimeAnomalyDetection.ipynb
```

Point the data path to your CSV, then run the cells; the streaming loop animates the detection.

---

<a name="-türkçe"></a>
## 🇹🇷 Türkçe

### Genel Bakış
Anomali tespiti, nadir olayların sorun işaret ettiği her yerde önemlidir — dolandırıcılık, ekipman arızası, ağ saldırısı. Bu proje bir **Isolation Forest** eğitir, ardından veriyi canlı bir akış gibi yeniden oynatıp her gelen noktayı skorlar ve görselleştirmeyi gerçek zamanlı günceller.

### Veri Seti
Sayısal özniteliklerden oluşan tablo verisi (Colab'da Google Drive'dan yüklenir); her satır gelen veri akışının bir "anı" olarak işlenir.

### Yaklaşım
1. **Ön işleme** — veri yüklenir, öznitelikler `StandardScaler` ile standartlaştırılır.
2. **Model** — rastgele bölmelerle aykırı değerleri izole eden gözetimsiz **Isolation Forest** eğitilir.
3. **Gerçek zamanlı simülasyon** — bir zamanlama döngüsüyle veride ilerlenir, noktalar tek tek skorlanır ve canlı grafik (`clear_output`) yenilenerek bir izleme panosu taklit edilir.
4. **Değerlendirme** — sonuçlar `classification_report` ve `confusion_matrix` ile özetlenir.

### Teknolojiler
`Python` · `pandas` · `numpy` · `scikit-learn` · `matplotlib` · `seaborn`

### Çalıştırma
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
jupyter notebook RealTimeAnomalyDetection.ipynb
```
Veri yolunu kendi CSV'ne ayarla ve hücreleri çalıştır; akış döngüsü tespiti canlandırır.
