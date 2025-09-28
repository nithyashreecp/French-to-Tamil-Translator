# French → Tamil Translator (5-letter words)

## 📌 Problem Statement
This project focuses on translating **5-letter French words into Tamil**.  
It was built as an extension of my training project, adding extra features such as:
- Multiple models (custom Seq2Seq vs pretrained Transformer)
- Interactive Gradio interface for live translation
- Visual evaluation metrics

## 📂 Dataset
- Source: `french_tamil_5letters.txt`  
- Format: `French_word → Tamil_word`  
- Only **5-letter French words** are used.  
- Dataset is preprocessed by lowercasing, splitting pairs, and padding sequences.

## 🛠 Methodology
1. **Preprocessing**  
   - Character-level tokenization for French and Tamil.  
   - Padding sequences to uniform length.  
   - Teacher forcing (decoder input shifted by one token).  

2. **Models**  
   - **Seq2Seq Model**: Embedding + LSTM encoder-decoder.  
   - **mBART-50**: Pretrained multilingual transformer from HuggingFace.  

3. **Interface**  
   - A Gradio app that allows users to input a French word and get its Tamil translation.  
   - Validates that only 5-letter French words are allowed.  

## 📊 Results
- **Seq2Seq model** trained for 10 epochs.  
- Validation accuracy and loss curves are included below.  
- **mBART-50** provides higher-quality translations without task-specific training.  

| Model       | Strengths                  | Weaknesses                  |
|-------------|---------------------------|-----------------------------|
| Seq2Seq LSTM| Learns custom dataset     | Needs more training data    |
| mBART-50    | Strong pretrained results | May not handle rare words   |

## 📈 Visualizations
- Training vs validation accuracy/loss plots  
- Sample translations table  
- Gradio app screenshots  

## 🚀 Usage
### Install requirements
```bash
pip install -r requirements.txt
