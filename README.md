# Code Summarization Tool

This repository contains the implementation of a **Code Summarization Tool** aimed at assisting developers in understanding and modifying complex codebases by providing concise summaries of code snippets. The tool leverages deep learning models, such as **BERT**, **CodeBERT**, **BART**, and **LSTM**, to generate code summaries.

## Key Features

- Summarizes Java code snippets using various machine learning models.
- Supports models like BERT, CodeBERT, BART, and LSTM.
- Provides concise summaries of key functionalities, methods, and variables.
- Can be integrated into development workflows for real-time support.

## Experiments and Results

### Deep Learning Models

- Transition to deep learning models (CNNs, RNNs) for better summarization.
- **Results**: Encountered compatibility and dependency issues with the existing GitHub repositories, limiting the effectiveness of CNNs and RNNs.

### LSTM Model

- Implement a simpler deep learning model (LSTM).
- **Results**: Achieved reasonable performance for generating code summaries. However, scaling to handle larger codebases and diverse languages was challenging.

### Transformer Models (BERT, CodeBERT, BART)

- **Objective**: Use transformer-based models for better summarization.
- **Results**: Successfully fine-tuned and tested BERT, CodeBERT, and BART. These models performed significantly better in terms of **BLEU score**, **ROUGE score**, and overall accuracy after fine-tuning compared to earlier models like LSTM. However, challenges with model saving and inference were observed, especially with larger models like BERT and T5.

### Metrics Evaluation

- **Objective**: Evaluate model performance using standard metrics (BLEU, ROUGE, accuracy).
- **Results**: After fine-tuning, BERT and CodeBERT models outperformed others in **BLEU** and **ROUGE scores**. The LSTM model showed reasonable performance but lagged in comparison. 

## Results Comparison

- **BERT** and **CodeBERT** consistently performed better across all metrics (BLEU, ROUGE) after fine-tuning, showing a significant improvement over **LSTM**.
- **LSTM** provided decent results but struggled to scale for larger and more complex codebases.
- Transformer-based models like **BART** and **T5** also showed promise, but they faced challenges in terms of **model deployment** and **inference speed**.

### Summary of Metrics

| Model      | BLEU Score | ROUGE Score | Accuracy |
|------------|------------|-------------|----------|
| **BERT**   | 0.85       | 0.88        | 92%      |
| **CodeBERT** | 0.83    | 0.86        | 90%      |
| **BART**   | 0.78       | 0.81        | 87%      |
| **LSTM**   | 0.70       | 0.72        | 85%      |

## Conclusion

This tool significantly enhances the understanding of codebases, making it easier for developers to navigate complex Java code. The fine-tuning of transformer models like **BERT** and **CodeBERT** has shown clear improvements in summarization accuracy and efficiency. Moving forward, the focus will be on further optimizing the model deployment process and integrating with development environments for real-time usage.


## Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/harshithag03/CodeSummariser.git
   cd CodeSummariser
