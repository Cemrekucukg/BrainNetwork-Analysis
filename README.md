# 🧠 EEG-Based Psychiatric Disorder Classification

This project focuses on classifying **psychiatric disorders** using EEG and QEEG data through **deep learning models**.  
By analyzing brain activity signals, it aims to identify neural patterns that distinguish healthy individuals from those diagnosed with psychiatric conditions.

## 📘 Overview
Electroencephalography (EEG) is a widely used neuroimaging method for recording brain electrical activity.  
In this study, EEG signals were processed and analyzed to classify psychiatric disorders using deep neural networks.  
The project demonstrates the potential of AI-assisted diagnostic tools in clinical applications.

Two main models were developed:
- **Multi-class model** – classifies multiple psychiatric disorders  
- **Binary model** – distinguishes between healthy and psychiatric groups  

## 📂 Dataset
The dataset contains EEG signals and clinical information from **945 participants** with **1149 features**.  
It includes:
- Demographics (age, gender, education, IQ)  
- Diagnosis labels (main disorder & specific subtypes)  
- EEG features: **Power Spectral Density (PSD)** and **Functional Connectivity (FC)**  

🧩 Key Challenges:  
- **Imbalanced classes** (some disorders underrepresented)  
- **High dimensionality** of EEG features  
- **Preprocessing** handled via normalization, encoding, and missing-value imputation  

## ⚙️ Methodology
### 🧪 Data Processing
- **One-hot encoding** for categorical variables  
- **StandardScaler** normalization for EEG data  
- **Train-test split** (80% / 20%)  
- **Weighted loss** to handle class imbalance  

### 🧠 Deep Learning Models
#### Model 1 – Multi-class Classification
- Fully connected neural network (1024 → 512 neurons)  
- ReLU activations, dropout (0.3)  
- Weighted cross-entropy loss  
- **Accuracy:** 25.40%  

#### Model 2 – Binary Classification
- Deep architecture (2048 → 1024 → 512 → 256 → 128 neurons)  
- Batch normalization + dropout (0.1)  
- Adam optimizer (lr=0.001)  
- Early stopping after 18 epochs  
- **Accuracy:** 83.60%  

## 📊 Results
| Model | Task | Accuracy |
|-------|------|-----------|
| Multi-class | All disorders | 25.40% |
| Binary | Healthy vs Disorder | 83.60% |

✅ The binary classification achieved strong performance, demonstrating the feasibility of EEG-based psychiatric screening.  
Further improvements can be achieved using **RNN**, **LSTM**, or **temporal CNN** architectures for sequence modeling.

## 🧰 Technologies
- Python  
- TensorFlow / Keras  
- NumPy, pandas, Scikit-learn  
- Matplotlib, Seaborn  

## 🚀 Run
```bash
pip install -r requirements.txt
jupyter notebook


 ##👩‍💻 Author

Cemre Küçükgöde
This project was developed for academic and research purposes as part of a deep learning study on EEG-based psychiatric disorder classification.
