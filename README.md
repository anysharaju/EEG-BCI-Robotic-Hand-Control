# 🧠 4-Class Motor Imagery BCI Classification

## ✨ Project Overview

This project implements a **Brain-Computer Interface (BCI)** system for classifying **four distinct motor imagery (MI)** tasks based on electroencephalography (EEG) data. It serves as an exploration into **Human-Computer Interaction (HCI)** by demonstrating how mental tasks can be translated into command signals.

The system uses the publicly available **BCI Competition IV Dataset 2a** to classify four imagined movements:

1.  **Left Hand**
2.  **Right Hand**
3.  **Foot**
4.  **Tongue**

## 🚀 Features

* **Dataset Handling:** Imports and concatenates multiple patient CSV files from the BCI Competition IV Dataset 2a.
* **Feature Extraction:** Extracts both **time-domain** (Mean, Variance) and **frequency-domain** features.
* **Power Spectral Density (PSD):** Uses **Welch's method** to calculate band power across 22 EEG channels for the following key frequency bands:
    * Delta ($\delta$): 0.5–4 Hz
    * Theta ($\theta$): 4–8 Hz
    * Alpha ($\alpha$): 8–13 Hz
    * Beta ($\beta$): 13–30 Hz
    * Gamma ($\gamma$): 30–50 Hz
* **Classification:** Employs a **Random Forest Classifier** (`sklearn.ensemble`) for multi-class prediction of the motor imagery task.
* **Performance Analysis:** Generates a detailed **Classification Report** and **Confusion Matrix** to evaluate the model's accuracy.

## 🛠️ Technical Details

### Dataset

* **Source:** BCI Competition IV Dataset 2a (`BCICIV_2a_csv.zip`)
* **Channels:** 22 EEG channels
* **Target Classes:** 4 classes ('left', 'right', 'foot', 'tongue')

### Programming Languages and Libraries

This project is written in **Python 3.x** and relies on the following core libraries:

| Library | Purpose |
| :--- | :--- |
| `pandas` | Data loading and manipulation of CSV files. |
| `numpy` | Fundamental array processing. |
| `scipy.signal` | PSD estimation using Welch's method. |
| `scikit-learn` | Machine learning (RandomForestClassifier, metrics, splitting). |
| `matplotlib`/`seaborn` | Visualization of results and feature distributions. |

## ⚙️ Setup and Installation

### 1. Requirements

* Python 3.7+
* The `BCICIV_2a_csv.zip` dataset must be downloaded and accessible (as configured in the Jupyter notebook).

### 2. Dependencies

Install all required libraries using pip:

```bash
pip install pandas numpy scipy scikit-learn matplotlib seaborn
