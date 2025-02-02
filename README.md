# Topsis on Pre-Trained AI models for conversational text

This project evaluates the performance of different AI chatbot models using NLP metrics such as **BLEU, ROUGE, and BERTScore**. It also ranks the models using the **TOPSIS multi-criteria decision-making method**.

## 🚀 Features
- Generates responses from multiple chatbot models.
- Computes **BLEU, ROUGE, and BERTScore** for evaluation.
- Implements **TOPSIS ranking** to determine the best model.
- Supports GPU acceleration for faster processing.
- Exports results as a CSV file and visualizes evaluation metrics.

## 📂 Setup Instructions
### 1️⃣ Install Dependencies
Run the following command in Google Colab or your local machine:
```sh
pip install transformers evaluate torch pandas numpy rouge_score bert_score seaborn matplotlib
```

### 2️⃣ Clone the Repository
```sh
git clone https://github.com/aryalal11/Topsis_Pretrained.git
cd Topsis_Pretrained
```

### 3️⃣ Run the Script
Open **Google Colab** or run the script locally:
```sh
python topsis_pretrained.py
```

## 🛠️ Usage
1. **Modify chatbot models** in the script:
```python
model_names = {
    "BlenderBot": "facebook/blenderbot-400M-distill",
    "DialoGPT": "microsoft/DialoGPT-small",
    "Falcon-RW": "tiiuae/falcon-rw-1b"
}
```
2. **Change evaluation references** if needed:
```python
reference = ["AI will impact healthcare, automation, finance, and more."]
```
3. **Run the script** and check results:
   - Final ranking will be displayed in the console.
   - A CSV file **(model_evaluation_results.csv)** will be saved.

## 📊 Visualizing the Results
The script generates bar plots for comparison:
```python
import seaborn as sns
import matplotlib.pyplot as plt
sns.barplot(x="Model", y="BLEU", data=df, palette="Blues")
plt.show()
```
![image](https://github.com/user-attachments/assets/c91d4709-1a74-4f00-a32b-7d1dae17b022)

## 🏆 Ranking using TOPSIS
The project applies **TOPSIS** to rank chatbot models based on:
- BLEU Score
- ROUGE Score
- BERTScore
- Latency (lower is better)

The final **TOPSIS Score** determines the best chatbot model.

## 🙌 Acknowledgments
- [Hugging Face Transformers](https://huggingface.co/transformers/)
- [Evaluate Library](https://huggingface.co/docs/evaluate/index)
- [TOPSIS Method](https://en.wikipedia.org/wiki/TOPSIS)

---
🎯 **Contributions Welcome!** Feel free to fork, improve, and submit PRs! 😊

