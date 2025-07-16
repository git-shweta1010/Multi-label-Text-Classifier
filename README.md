
# 🧠 Multi-Task NLP Model using LSTM

This project implements a **Multi-Task Learning (MTL)** approach using LSTM to simultaneously perform multiple related natural language processing tasks: **Emotion Detection**, **Violence Detection**, and **Hate Speech Classification**.

> Multi-Task Learning (MTL) is a machine learning approach where a model is trained on **multiple tasks simultaneously**, leveraging shared representations to improve generalization.

## 🛠️ Libraries Used

- `Pandas`, `NumPy` – data manipulation
- `Scikit-learn` – evaluation and preprocessing
- `NLTK` – text cleaning and stopword removal
- `TensorFlow / Keras` – model building
- `Seaborn`, `Matplotlib` – data visualization

## 🧱 Model Architecture

The model follows a shared-core MTL design:

### ⚙️ Components

1. **Individual Inputs**  
   Each task (Emotion, Violence, Hate) has its own input.

2. **Shared Core Layers**  
   - **Embedding Layer**
   - **LSTM Layer**
   - **Dropout and Pooling Layers**  
   These layers are **shared** across all tasks to learn a common representation.

3. **Individual Output Layers**  
   Each task has its own output head with a softmax activation to make separate predictions.

## 🔍 Tasks Performed

- 🧑‍🎤 **Emotion Classification**  
  (e.g., joy, sadness, anger, fear, etc.)

- 🔪 **Violence Type Detection**  
  (e.g., emotional, sexual, economic violence, etc.)

- 🚫 **Hate Speech Detection**  
  (e.g., offensive, hate speech, or neutral)

## 📊 Datasets Used

| Task         | Dataset | Link |
|--------------|---------|------|
| Emotion      | [Emotions Dataset (Kaggle)](https://www.kaggle.com/datasets/nelgiriyewithana/emotions) |
| Violence     | [Gender-based Violence Tweet Classification](https://www.kaggle.com/datasets/gauravduttakiit/gender-based-violence-tweet-classification?select=Train.csv) |
| Hate Speech  | [Hate Speech and Offensive Language Dataset](https://www.kaggle.com/datasets/mrmorj/hate-speech-and-offensive-language-dataset) |

## 📂 Project Structure

```
Multi-Task-NLP/
├── Final_Project.ipynb         # Main Jupyter notebook
├── Train.csv                   # Violence dataset
├── labeled_data.csv            # Hate speech dataset
├── text_data.csv               # Emotion dataset
├── README.md                   # Project documentation
└── data/                       # (Optional) Folder for large or external datasets
```

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Multi-label-Text-Classifier.git
   cd Multi-label-Text-Classifier
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Open the notebook:
   ```bash
   jupyter notebook Final_Project.ipynb
   ```

4. Run all cells to train and test the multi-task model.

## 📈 Example Output

```text
Input: "They always ignore my pain and make fun of my emotions."

Major Label: Emotion  
Sub Label: Sadness
```

