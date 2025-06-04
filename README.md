
# Finetune HR Sentiment

This project fine-tunes a Hugging Face transformer model to classify employee survey responses into sentiment categories like:

- **Disengaged**
- **Engaged**
- **Content**
- **At Risk of Leaving**

Built with:
- Hugging Face Transformers
- Weights & Biases (W&B) for hyperparameter sweeps
- Custom labeled dataset from employee reviews

---

## Features

- Fine-tunes a base transformer model (e.g. BERT or DistilBERT)
- Performs multi-class classification using softmax
- Evaluates using macro/weighted F1, accuracy
- Saves and logs best models per sweep run
- Easily re-loadable for inference or transfer

---

## Project Structure

```
.
├── train_sentiment_model.ipynb   # Core notebook: training + sweeps
├── test.csv                      # Test dataset (text, label)
└── README.md
```

---

## How to Run

1. Install dependencies:
   ```bash
   pip install transformers datasets wandb scikit-learn
   ```

2. Set your W&B project:
   ```python
   import wandb
   wandb.init(project="hr-sentiment")
   ```

3. Run the notebook: `train_sentiment_model.ipynb`

4. Evaluate using your own test file:
   ```python
   test.csv  # with 'text' and 'label' columns
   ```

---
