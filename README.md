# 🚀 Text Classification using Attention Mechanism 📝

## 📚 Overview

This project aims to perform **text classification** using an attention mechanism implemented in **Python** with **PyTorch**. The attention mechanism allows the model to focus on specific parts of the input text, improving its performance in understanding and classifying text data.

## 🛠️ Tools and Technologies Used

- **Programming Language**: `Python`
- **Deep Learning Framework**: `PyTorch`
- **Libraries**:
  - `numpy`
  - `pandas`
  - `tqdm`
  - `nltk`
  - `scikit-learn`

## 📊 Dataset

The dataset used for this project is a collection of consumer complaints, where each complaint is labeled with a specific product category. The dataset is stored in a CSV file (`complaints.csv`).

## 🔄 Preprocessing

### GloVe Embeddings

- The pre-trained GloVe word embeddings are used to represent words in the text data.
- The embeddings are processed from the `glove.6B.50d.txt` file.
- The vocabulary and embeddings are saved as pickle files (`vocabulary.pkl` and `embeddings.pkl`).

### Text Data Processing

- The text data is loaded from the CSV file.
- Missing values are dropped, and product labels are mapped to predefined categories.
- Text preprocessing includes converting to lowercase, removing punctuation and digits, and tokenization.
- Tokens are indexed using the vocabulary, and sequences are padded or truncated to a fixed length.

## 🧠 Model Architecture

### Attention Model

- The attention mechanism is implemented as a PyTorch module.
- It calculates attention weights based on input embeddings and applies them to the input data.
- The attention-weighted input is passed through a linear layer to obtain class predictions.

## 🚀 Training

- The model is trained using a custom PyTorch dataset.
- Training is performed for a specified number of epochs with mini-batch gradient descent.
- Training and validation loss are monitored to prevent overfitting.
- The best model is saved based on validation loss.

## 📈 Evaluation

### Testing

- The trained model is evaluated on a separate test dataset.
- Test loss and accuracy are calculated to assess model performance.

## 🎯 Inference

### Prediction on New Text

- The trained model can be used to make predictions on new text data.
- Input text is preprocessed and converted into tokens and integer indices.
- The model predicts the class label for the input text.

## 🏁 Conclusion

This project demonstrates the effectiveness of using an attention mechanism for text classification tasks. By focusing on relevant parts of the input text, the attention model achieves improved accuracy in categorizing consumer complaints into predefined product categories.
