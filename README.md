# PyCaret Assignments — Data Mining Project

This repository contains all deliverables for the Data Mining class assignment based on **PyCaret** (Low-Code Machine Learning).  
Each task is implemented, executed, and explained in an organized set of notebooks with results, plots, and video demonstrations.

---

## 📂 Repository Structure

```
pycaret-assignments/
│
├── env/                         # Environment files
│   └── core_requirements.txt     # Dependencies for PyCaret 3.x tasks
│   └── requirements_pycaret23.txt # For Association Rules (PyCaret 2.3.5)
│
├── notebooks/                   # All main tasks
│   ├── 01_binary_classification.ipynb
│   ├── 02_multiclass_classification.ipynb
│   ├── 03_regression.ipynb
│   ├── 04_clustering.ipynb
│   ├── 05_anomaly_detection.ipynb
│   ├── 06_association_rules_pycaret_2_3_5.ipynb
│   ├── 07_ts_univariate_no_exog.ipynb
│   └── 08_ts_univariate_with_exog.ipynb
│
├── gradio/                      # Interactive demo apps
│   ├── clf_demo.py              # Bank Marketing classifier demo
│   └── reg_demo.py              # Auto MPG regression demo
│
├── media/
│   ├── Anomaly Detection
│   ├── Association Rules Mining
│   ├── Binary Classification
│   ├── Clustering
│   ├── Multiclass Classification
│   ├── Regression
│   ├── Time Series Forecasting - Univariate with Exogenous Variables
│   ├── Time Series Forecasting - Univariate without Exogenous Variables                
│   └── VideosURL                 
│                     
└── README.md          
```

---

## 🧠 Tasks Implemented

| # | Task | Dataset Used | Notes |
|---|------|---------------|-------|
| 1 | **Binary Classification** | UCI Bank Marketing (Additional) | AutoML with GPU; evaluated via F1, ROC, PRC plots |
| 2 | **Multiclass Classification** | Palmer Penguins | 3-class species prediction |
| 3 | **Regression** | Auto MPG | Predicted car fuel efficiency |
| 4 | **Clustering** | Mall Customers | KMeans clustering + t-SNE visualization |
| 5 | **Anomaly Detection** | Synthetic Credit Fraud (3 000 rows) | Isolation Forest |
| 6 | **Association Rules** | Groceries basket (PyCaret 2.3.5) | Apriori rules (support, confidence, lift) |
| 7 | **Time Series – Univariate (No Exogenous)** | Daily Minimum Temperatures | 14-day forecasting |
| 8 | **Time Series – Univariate (With Exogenous)** | Synthetic retail-like data | Weekly + promo + holiday features |

---

## ⚙️ Environment Setup

### For PyCaret 3.x tasks
```bash
pip install -r env/core_requirements.txt
# or directly
pip install "pycaret==3.3.2" "gradio>=4.44,<5" "huggingface_hub<0.26.0"
```

### For Association Rules (PyCaret 2.3.5)
```bash
pip install -r env/requirements_pycaret23.txt
# or directly
pip install "pycaret==2.3.5" "mlxtend>=0.22"
```

---

## 🚀 Running the Notebooks

Each notebook runs standalone on **Kaggle or Google Colab**.

1. Turn **GPU** on (Runtime → Change runtime type → GPU).  
2. Run all cells top-to-bottom.  
3. Outputs are automatically saved to:
   ```
   /kaggle/working/media/figures/
   /kaggle/working/notebooks/
   ```

---

## 🌐 Gradio Demos

Two short interactive apps demonstrate model inference:

| Demo | File | Model | Description |
|------|------|--------|--------------|
| **Binary Classifier** | `gradio/clf_demo.py` | `binclf_final.pkl` | Predict if a customer subscribes (Bank Marketing) |
| **Regression** | `gradio/reg_demo.py` | `regression_mpg_final.pkl` | Predict car MPG using Auto MPG data |

Run in Kaggle / Colab:
```bash
!pip install gradio
!python gradio/clf_demo.py
```
A public `.gradio.live` URL will appear for testing and recording.

---

## 🎥 Video Demonstrations

All video walkthroughs URLS are located in  
`media/VideosURL`.  
Each clip shows the dataset load, setup, AutoML, plots, and final results.  
Two extra clips demonstrate **Gradio apps** (Binary & Regression).

---

## 👩‍💻 Author

**Prachi G.**  
Data Mining Course Assignment — 2025 

---

**✅ Ready to run, reproduce, and grade.**
