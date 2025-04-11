##  Overview

This project explores and compares three different deep learning models for **image captioning**, a task at the intersection of computer vision and natural language processing where the goal is to generate descriptive captions for images.

The models analyzed include:

1. **CNN-RNN Model**  
   A custom-built convolutional neural network (CNN) for visual feature extraction, combined with an LSTM-based language model.

2. **VGG16-RNN Model**  
   A model that leverages the **pre-trained VGG16** network as a visual encoder, feeding features into an LSTM-based decoder for caption generation.

3. **Transformer-based Model**  
   A modern architecture using **Swin Transformer** for vision encoding and **GPT-2** for natural language generation.

---

## Dataset Used

The models were trained and evaluated on the **Flickr8k dataset**, which contains:

- **8,000 images**
- **5 captions per image** written by humans

---

## Key Findings

- The **Transformer-based model** outperformed the others, producing more **accurate and coherent** image descriptions.
- The **CNN-RNN** and **VGG16-RNN** models generated **repetitive or less relevant** captions.
- Performance was quantitatively assessed using the **BLEU score** (a metric for evaluating generated text against reference captions):

| Model             | BLEU Score |
|------------------|------------|
| CNN-RNN          | ~0.36      |
| VGG16-RNN        | ~0.38      |
| Transformer Model| ~0.60–0.80 |

## Conclusion

- **Transformer models** show clear advantages in image captioning tasks, particularly due to their **self-attention mechanisms**, which allow them to generate richer and more context-aware captions.
- **CNN-based models** can still be effective but may benefit from:
  - Improved visual feature extraction
  - Access to larger and more diverse datasets
