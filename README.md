# Fake-Fingerprint

# 🕵️ Fake Fingerprint Detection using DefraudNet

This project implements a deep learning-based system for detecting **fake (spoofed) fingerprints** using **DefraudNet**, a specialized Convolutional Neural Network (CNN) architecture designed for fraud detection. The model classifies fingerprint images as either **real** or **fake**, helping to enhance biometric security systems.

---

## 📌 Overview

Biometric authentication systems, particularly those using fingerprints, are prone to spoofing attacks with artificial fingerprints. This project adapts the **DefraudNet** architecture to detect such fraudulent inputs based on fingerprint images.

---

## 🧠 What is DefraudNet?

**DefraudNet** is a lightweight CNN architecture designed for fraud detection tasks. It provides a balance between performance and computational efficiency, making it well-suited for applications where real-time or edge deployment is necessary.

---

## 📂 Project Structure

Fake-Fingerprint/
├── data/ # Dataset folder containing 'real/' and 'fake/' subfolders
├── models/ # Trained model weights and checkpoints
├── utils/ # Utility scripts (preprocessing, metrics, etc.)
├── defraudnet.py # DefraudNet architecture implementation
├── main.py # Entry point for training and testing
├── requirements.txt # Required Python packages
└── README.md # Project documentation


---

## 🖼️ Dataset Format

Organize your dataset like this:

data/
├── real/
│ ├── real1.png
│ ├── real2.png
│ └── ...
└── fake/
├── fake1.png
├── fake2.png
└── ...


> **Note:** You can use datasets like **LivDet**, or custom datasets with labeled real and fake fingerprint images.

---

## 🔧 Installation

### 1. Clone the Repository

git clone https://github.com/arpit2764/Fake-Fingerprint.git
cd Fake-Fingerprint

### 2.Create a Virtual Environment (optional but recommended)
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate

### 3.Install Dependencies
pip install -r requirements.txt

**🚀 How to Use**
__🏋️‍♀️ Train the Model__

python main.py --mode train --data_dir ./data/

**🧪 Test the Model on a Single Image**
python main.py --mode test --image_path ./path_to_image.png

**📝 Command-Line Arguments**
| Argument       | Description                                   | Example                              |
| -------------- | --------------------------------------------- | ------------------------------------ |
| `--mode`       | Operation mode: `train` or `test`             | `--mode train`                       |
| `--data_dir`   | Path to dataset folder                        | `--data_dir ./data/`                 |
| `--image_path` | Path to image file (used only in `test` mode) | `--image_path ./img/fingerprint.png` |


**📊 Example Results**
| Metric    | Score |
| --------- | ----- |
| Accuracy  | 95.4% |
| Precision | 94.2% |
| Recall    | 96.1% |
| F1 Score  | 95.1% |

**🛠️ Future Improvements**
Integrate support for real-time fingerprint scanners.

Train on larger and more diverse datasets (e.g., multiple spoofing materials).

Extend model to other biometric modalities (e.g., face, iris).


**🐛 Known Limitations**
May struggle with poor quality or noisy fingerprint images.

Dataset imbalance can affect classification performance.

**📜 License**
This project is licensed under the MIT License. See the LICENSE file for more details.

**👤 Author**
Arpit2764
GitHub: @arpit2764

**🙌 Acknowledgments**
The creators of DefraudNet for the base architecture.

Public biometric datasets like LivDet for training and evaluation.
