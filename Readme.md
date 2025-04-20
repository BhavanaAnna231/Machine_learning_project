# Neural Conversational Agent

## Overview

This project implements a sequence-to-sequence based chatbot using the Cornell Movie Dialog Corpus. The implementation includes detailed theory, mathematical formulations, and complete code for building a neural conversational agent capable of generating human-like responses.

## Features

- **Comprehensive Theory**: Detailed explanations of neural language models, RNNs, LSTMs, and sequence-to-sequence architectures
- **Mathematical Foundations**: Formulas for attention mechanisms, encoder-decoder architectures, and LSTM gates
- **Memory-Efficient Implementation**: Optimized for systems with limited resources
- **Interactive Demo**: Streamlit application for demonstrating the chatbot's capabilities

## Key Components

1. **Data Preprocessing Pipeline**
   - Automatic dataset download using kagglehub
   - Text cleaning and normalization
   - Filtering by sequence length
   - Tokenization and sequence conversion

2. **Model Architecture**
   - Bidirectional LSTM encoder
   - LSTM decoder
   - Pre-trained GloVe word embeddings (50-dimensional)
   - Memory-efficient sparse categorical cross-entropy loss

3. **Training and Evaluation**
   - Early stopping to prevent overfitting
   - Learning rate reduction on plateau
   - Memory-optimized batch processing

4. **Interactive Testing**
   - Command-line interface for real-time conversation
   - Streamlit web application for demonstration

## Installation

1. Clone this repository:
```
git clone https://github.com/BhavanaAnna231/Machine_learning_project
cd Machine_learning_project
```

## Dataset

This project uses the Cornell Movie Dialog Corpus, containing over 220,000 conversation exchanges between more than 10,000 movie characters. The dataset is automatically downloaded using:

```python
kagglehub.dataset_download("agsam23/movie-dialogs")
```

## Memory Optimization

The implementation is optimized for systems with limited resources:
- Reduced vocabulary size (5,000 words)
- Smaller sample size (2,000 conversations)
- Shorter sequence length (12 words maximum)
- Efficient memory management with garbage collection
- Reduced model complexity (64 hidden units)
- Sparse categorical cross-entropy to avoid one-hot encoding

## Usage

### Jupyter Notebook

To explore the complete implementation with theory and code:
```
jupyter notebook index.ipynb
```

## References

- Sutskever, I., Vinyals, O., & Le, Q. V. (2014). Sequence to sequence learning with neural networks.
- Bahdanau, D., Cho, K., & Bengio, Y. (2014). Neural machine translation by jointly learning to align and translate.
- Luong, M. T., Pham, H., & Manning, C. D. (2015). Effective approaches to attention-based neural machine translation.
