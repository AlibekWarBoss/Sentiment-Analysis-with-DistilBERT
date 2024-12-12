
# Sentiment Analysis with DistilBERT

![Python](https://img.shields.io/badge/Python-3.10-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.5.1-orange)
![License](https://img.shields.io/badge/License-MIT-green)

## Overview

This project demonstrates sentiment analysis using **DistilBERT**, a lightweight transformer model, on the **IMDb dataset**. The primary goal is to classify movie reviews as **positive** or **negative**, focusing on computational efficiency and model accuracy. 

Key features include:
- Gradient checkpointing for memory optimization.
- Mixed precision training for faster computations.
- Data augmentation techniques to improve generalization.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributors](#contributors)
- [License](#license)

## Features

- **Model**: DistilBERT for sequence classification with two output classes (positive/negative).
- **Optimization**: Mixed precision training and AdamW optimizer for better performance.
- **Augmentation**: Enhanced the dataset with paraphrasing and noise injection.
- **Metrics**: Accuracy and F1-score used for evaluation.

## Dataset

The project uses the IMDb dataset:
- **Training Data**: 25,000 labeled reviews (positive and negative).
- **Test Data**: 25,000 labeled reviews (positive and negative).

Dataset source: [IMDb Dataset](https://ai.stanford.edu/~amaas/data/sentiment/)

## Installation

### Prerequisites
Ensure you have the following installed:
- Python 3.10 or above
- PyTorch with CUDA (if GPU is available)
- Other required libraries specified in `requirements.txt`.

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/sentiment-analysis-distilbert.git
   cd sentiment-analysis-distilbert
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Download and prepare the IMDb dataset:
   ```bash
   wget https://ai.stanford.edu/~amaas/data/sentiment/aclImdb_v1.tar.gz
   tar -xvzf aclImdb_v1.tar.gz
   ```

4. Run the project notebook in Jupyter or VSCode.

## Usage

1. Train the model:
   - Open the `notebooks/upemoa.ipynb` file.
   - Follow the steps to preprocess the data, train the model, and evaluate it.

2. Evaluate the model:
   - The evaluation results, including accuracy and F1-score, are printed in the notebook.

3. Visualize the results:
   - Refer to the classification report and confusion matrix provided in the notebook.

## Results

| Model                         | Accuracy | F1-Score |
|-------------------------------|----------|----------|
| Logistic Regression (Baseline)| 85.2%    | 84.5%    |
| DistilBERT (No Augmentation)  | 88.5%    | 88.1%    |
| DistilBERT (With Augmentation) | 89.8%    | 89.5%    |

## Contributors

- **Your Name** - Implementation, model training, and evaluation.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
