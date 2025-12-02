### Gold Headline Sentiment Classifier

This project is a lightweight Natural Language Processing (NLP) tool designed to classify financial news headlines regarding the gold market into **Positive** or **Negative** sentiments.

---

### Key Features

* **Ultra-Lightweight Model:** Utilizes `prajjwal1/bert-tiny`, a compact version of BERT designed to run efficiently on devices with limited resources while maintaining reasonable accuracy.
* **Uncertainty Detection:** The model includes a logic filter that flags predictions with a confidence score below **75%** as "uncertain".
* **Interactive Interface:** Features a user loop that allows you to type in custom headlines and receive real-time sentiment predictions.

Here are the specific requirements extracted from the code imports and file usage. You can copy this block into a `requirements.txt` file or add it to the README.

### Prerequisites

To run this project, you will need the following Python libraries installed:

  * **pandas** (Data manipulation)
  * **numpy** (Numerical operations)
  * **torch** (PyTorch deep learning framework)
  * **transformers** (Hugging Face model utilities)
  * **scikit-learn** (Data splitting and metrics)

### `requirements.txt`

```text
pandas
numpy
torch
transformers
scikit-learn
```

### Data Requirement

  * **gold-dataset.csv**: You must have a CSV file named `gold-dataset.csv` in the root directory containing columns for 'News' and 'Price Sentiment'.


### How It Works

1.  **Data Loading:** The script reads the csv, filters for positive/negative sentiments, and splits the data into training and validation sets.
2.  **Training:** The model trains for **6 epochs** with a learning rate of `2e-5` and a batch size of `32`.
3.  **Prediction:** After training, the script enters a loop where you can input text (e.g., "Gold is gonna go up today!") and receive a classification with a confidence percentage.

### Usage

1.  Ensure `gold-dataset.csv` is present.
2.  Run all cells in the Jupyter Notebook.
3.  Scroll to the final cell to interact with the model.
4.  Type `quit` to exit the application.

---
