# Self-Supervised Learning for Image Classification

## Overview
This project investigates the effectiveness of **self-supervised learning (SSL)** methods for image classification, particularly in scenarios where labeled data is scarce. Traditional supervised learning requires large labeled datasets, which can be expensive and time-consuming to create. SSL provides an alternative by leveraging patterns from unlabeled data to build robust models.

We focus on two prominent SSL approaches:  
- **SimCLR** (Simple Framework for Contrastive Learning of Visual Representations)  
- **RotNet** (Rotation Prediction Network)  

Both are evaluated individually and in combination on the CIFAR-10 dataset under semi-supervised conditions (1%, 10%, and 50% of labeled data available).

---

## Objectives
- Evaluate robustness of SimCLR and RotNet under different levels of labeled data.  
- Explore hybrid modeling, combining SimCLR and RotNet to leverage their complementary strengths.  
- Compare against supervised learning baselines to assess SSL’s effectiveness when labeled data is limited.  

---

## Key Findings
- **SimCLR and RotNet consistently outperform supervised baselines** in low-label scenarios.  
- When combined, their conflicting objective functions (contrastive vs. rotation prediction) reduce overall effectiveness, as their feature spaces diverge.  
- Hybrid approaches show potential when carefully balanced, suggesting opportunities in dynamically weighting contributions.  

---

## Dataset
- **CIFAR-10** image dataset  
- Semi-supervised splits: 1%, 10%, and 50% labeled  

---

## Methods
- **SimCLR**: Learns representations by maximizing agreement between differently augmented views of the same image.  
- **RotNet**: Learns by predicting the degree of rotation applied to images (0°, 90°, 180°, 270°).  
- **Hybrid model**: Shared encoder + weighted joint loss to combine both approaches.  
