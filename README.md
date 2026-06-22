# 🚨 Real-Time Anomaly Detection — Credit Card Fraud

Catching fraudulent transactions in a **simulated live stream** with Isolation Forest, on a 284K-transaction dataset where only **0.17%** are fraud.

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-IsolationForest-orange.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626.svg)

**🌐 Language:** English · [Türkçe](#-türkçe)

## ⚡ Overview

Fraud is **rare and unlabeled in the moment**, which makes it a natural fit for *unsupervised* anomaly detection. This project trains an **Isolation Forest** on normal transactions, then replays the data as a live stream — flagging suspicious transactions as they "arrive", like a real monitoring system.

## 📊 Dataset

**Credit Card Fraud Detection** (`creditcard.csv`): **284,807 transactions × 31 columns**, extremely imbalanced — **284,315 normal vs 492 fraud (0.17%)**. Features `V1`–`V28` are PCA-anonymized; `Time` and `Amount` are standardized into `scaled_time` / `scaled_amount`.

## 🧠 Approach

1. **Preprocessing** — scale `Time` and `Amount` with `StandardScaler`, drop the originals.
2. **Model** — **Isolation Forest** (100 trees, `contamination=0.01`), fit on **normal transactions only** so anything that doesn't look normal is flagged.
3. **Real-time simulation** — stream rows one at a time with a timing loop, scoring each point and refreshing a live plot (`clear_output`) to mimic a monitoring dashboard.
4. **Evaluation** — `classification_report` and `confusion_matrix` against the true labels.

## 🛠️ Tech Stack

`Python` · `pandas` · `numpy` · `scikit-learn` (IsolationForest, StandardScaler, metrics) · `matplotlib` · `seaborn`

## ▶️ How to Run

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
jupyter notebook RealTimeAnomalyDetection.ipynb
```

Point the `creditcard.csv` path to your copy of the dataset, then run the cells; the streaming loop animates the detection.

---

<a name="-türkçe"></a>
## 🇹🇷 Türkçe

### Genel Bakış
Dolandırıcılık **nadirdir ve o an etiketsizdir** — bu da onu *gözetimsiz* anomali tespiti için doğal bir aday yapar. Bu proje normal işlemler üzerinde bir **Isolation Forest** eğitir, ardından veriyi canlı bir akış gibi yeniden oynatarak şüpheli işlemleri "geldikçe" işaretler.

### Veri Seti
**Credit Card Fraud Detection** (`creditcard.csv`): **284.807 işlem × 31 sütun**, aşırı dengesiz — **284.315 normal, 492 dolandırıcılık (%0,17)**. `V1`–`V28` öznitelikleri PCA ile anonimleştirilmiş; `Time` ve `Amount` standartlaştırılarak `scaled_time` / `scaled_amount` üretilir.

### Yaklaşım
1. **Ön işleme** — `Time` ve `Amount`, `StandardScaler` ile ölçeklenir, orijinaller atılır.
2. **Model** — **Isolation Forest** (100 ağaç, `contamination=0.01`), **yalnızca normal işlemler** üzerinde eğitilir; normale benzemeyen her şey işaretlenir.
3. **Gerçek zamanlı simülasyon** — satırlar bir zamanlama döngüsüyle tek tek akıtılır, her nokta skorlanır ve canlı grafik (`clear_output`) yenilenerek izleme panosu taklit edilir.
4. **Değerlendirme** — gerçek etiketlere karşı `classification_report` ve `confusion_matrix`.

### Teknolojiler
`Python` · `pandas` · `numpy` · `scikit-learn` · `matplotlib` · `seaborn`

### Çalıştırma
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
jupyter notebook RealTimeAnomalyDetection.ipynb
```
`creditcard.csv` yolunu kendi veri kopyana ayarla ve hücreleri çalıştır; akış döngüsü tespiti canlandırır.
