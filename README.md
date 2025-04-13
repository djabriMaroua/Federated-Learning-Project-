# 🧠 Federated Learning on the MIMIC-III Dataset

This project explores the use of **Federated Learning** for predicting **patient mortality** in Intensive Care Units (ICUs) using the **MIMIC-III clinical dataset**.

## 🎯 Objectives

- Perform **supervised classification** to predict mortality outcomes.
- Implement **non-IID data distribution** across multiple simulated clients (e.g., hospitals).
- Compare performance between a **federated model** and a **centralized model**.

---

## 📁 Project Structure

- `data/` : Contains raw CSV files extracted from MIMIC-III (e.g., `CHARTEVENTS.csv`, `LABEVENTS.csv`, etc.)
- `client_{i}_data.csv` : Partitioned non-IID data for each client.
- `final_dataset_with_mortality.csv` : Final dataset including mortality labels.
- `non_iid_distribution.png` : Visualization of data distribution across clients.
- `federated_vs_centralized_performance.png` : Side-by-side performance comparison.
- `bdm_federated_learning_mimic_iii.py` : Main script containing the full pipeline.

---

## ⚙️ Technologies Used

- Python (NumPy, Pandas, Matplotlib)
- PyTorch
- Scikit-learn
- Google Colab
- MIMIC-III Dataset (via PhysioNet)

---

## 🧪 Project Pipeline

1. **Data Preprocessing**
   - Extraction of key clinical features (e.g., GCS, vital signs, PaO₂/FiO₂, urine output, lab results)
   - Cleaning and handling of missing/outlier values

2. **Label Engineering**
   - In-hospital mortality
   - 48-hour ICU mortality
   - 30-day post-discharge mortality

3. **Federated Learning Implementation**
   - Non-IID partitioning across 10 clients
   - Local neural networks trained independently
   - Federated Averaging (FedAvg) for global model updates
   - Performance monitoring + **early stopping**

4. **Evaluation & Visualization**
   - Local and global model accuracy
   - Loss and accuracy curves per round
   - Comparison against a centralized model

---

## 📊 Results

- **Federated Model**:
  - Aggregates local client updates using FedAvg
  - Achieves competitive test accuracy across clients

- **Centralized Model**:
  - Trained on combined data for baseline comparison

Visualizations showcase class distributions, training dynamics, and final performance comparisons.

---

## ▶️ Demonstration Video

Watch a quick walkthrough of the project here:  
👉 [Project Demo (Google Drive)](https://drive.google.com/drive/folders/1qYIb8HzRgdzDV5BshhWqXL1WwGdnmzxq)

---

## 🚀 How to Run

1. Download the MIMIC-III dataset and upload it to Google Drive
2. Run the `bdm_federated_learning_mimic_iii.py` script on **Google Colab**
3. Outputs and plots will be saved automatically

---

## 👩‍💻 Author

- Developed by **[DJABRI Maroua ,BOUYAHIAOUI Meriem , DINARI Yasmine ,REZZOUG Aicha]** as part of the **Big Data Mining** course project
- Dataset used: [MIMIC-III Clinical Database](https://mimic.physionet.org/)

---

 
---
