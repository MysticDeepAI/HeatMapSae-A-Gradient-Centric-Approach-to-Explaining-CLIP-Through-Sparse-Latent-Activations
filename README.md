# Interpretability of CLIP with Sparse AutoEncoders and Gradient-Based Visualization

Link: [1 Part - Publication LessWrong](https://www.lesswrong.com/posts/9rG9xkrdi9ndPBiaE/part-1-enhancing-inner-alignment-in-clip-vision-transformers)

This project investigates the interpretability of CLIP by combining gradient-based visualization methods (heatmaps) with Sparse AutoEncoders (SAEs) trained on intermediate layers of the Vision Transformer (ViT) architecture. Our goal is to understand how specific latent features, captured by the SAE in a chosen CLIP layer (e.g., layer 22 residual), correlate with and influence the regions highlighted by gradient-derived heatmaps.

By manipulating sparse latent activations—either zeroing out certain features or amplifying them—we observe how these changes affect the final heatmaps. This sheds light on which latent dimensions drive the model’s attention and similarity scores. Our approach provides a more granular view of CLIP's internal representations and highlights potentially meaningful sub-circuits within the network, contributing to mechanistic interpretability research.

## Key Points

### Sparse Latent Coding
- **Sparse AutoEncoders (SAEs):** We train or utilize pre-trained SAEs that compress the high-dimensional activation space in CLIP’s intermediate layers into a latent representation with a small set of active features.

### Gradient-Based Heatmaps
- **Saliency Maps:** We generate heatmaps by backpropagating a gradient-derived score (e.g., image–text similarity) through the CLIP model. These heatmaps reveal which image regions are most crucial for CLIP’s decision or attention.

### Intervention & Analysis
- **Latent Feature Manipulation:** By modifying selected latent features (e.g., setting them to zero or scaling them) and reinjecting the reconstructed activations into CLIP, we can observe direct causal effects on the resulting heatmaps.

### Interpretability Insights
- **Localized Effects:** Preliminary results suggest certain latent features have strong, localized effects on attention maps. This helps attribute specific patches or concepts to particular directions in the SAE’s latent space.

## Why It Matters

### Mechanistic Interpretability
- **Beyond Feature Attribution:** This project advances interpretability by examining how explicit latent factors in an autoencoder framework interplay with gradient saliency.

### Actionable Explanations
- **Fine-Grained Control:** Fine-tuning sparse latent activations may enable targeted manipulation and provide a deeper conceptual understanding of CLIP’s internal circuits.



<!--## Acknowledgements-->

<!--*(Optional: Acknowledge contributors or resources)*-->

---
