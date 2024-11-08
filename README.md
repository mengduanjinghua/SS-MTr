# SS-MTr

[IEEE paper](https://ieeexplore.ieee.org/document/10106123)  |  [ResearchGate(Full Text Available)](https://www.researchgate.net/publication/370165081_Spectral-Spatial_Masked_Transformer_with_Supervised_and_Contrastive_Learning_for_Hyperspectral_Image_Classification)

This repo hosts the offical implementation for the paper: **Spectral–Spatial Masked Transformer With Supervised and Contrastive Learning for Hyperspectral Image Classification**, *IEEE Transactions on Geoscience and Remote Sensing (TGRS), Lingbo Huang, Yushi Chen, and Xin He*, including `SS-MTr`, `C-SS-MTr`, `S-SS-MTr`, and `SC-SS-MTr` for HSI classification

# Introduction

Recently, due to the powerful capability at modeling the long-range relationships, Transformer-based methods have been widely explored in many research areas, including hyperspectral image (HSI) classification. However, because of lots of trainable parameters and the lack of inductive bias, it is difficult to train a Transformer-based HSI classifier, especially when the number of training samples is limited. To address this issue, in this study, spectral–spatial masked Transformer (SS-MTr) is explored for HSI classification, which uses a two-stage training strategy. In the first stage, SS-MTr pretrains a vanilla Transformer via reconstruction from masked HSI inputs, which embeds the local inductive bias into the Transformer. In the second stage, the well pretrained Transformer is cooperated with a fully connected layer and is then fine-tuned for the HSI classification. Furthermore, in order to incorporate discriminative feature learning into the SS-MTr, three SS-MTr-based methods, including contrastive SS-MTr (C-SS-MTr), supervised SS-MTr (S-SS-MTr), and supervised C-SS-MTr (SC-SS-MTr), are proposed by adding extra branches for specific tasks in parallel with the existing reconstruction task. Specifically, the proposed C-SS-MTr adds a contrastive loss, which brings instance discriminability. Besides, the proposed S-SS-MTr builds an extra classification branch for embracing interclass discriminability and intraclass similarity. Moreover, the proposed SC-SS-MTr combines C-SS-MTr and S-SS-MTr for better generalization. The proposed SS-MTr, C-SS-MTr, S-SS-MTr, and SC-SS-MTr are tested on three popular hyperspectral datasets (i.e., Indian Pines, Pavia University, and Houston). The obtained results reveal that the proposed models achieve competitive results compared with the state-of-the-art HSI classification methods.

![figure](https://github.com/user-attachments/assets/4ad92439-1789-4934-9571-18a6d51512a5)

# Training

- `SS-MTr_main.py`: the main function for the model: SS-MTr.

- `C-SS-MTr_main.py` is the main function for the model: C-SS-MTr.

- `S-SS-MTr_main.py` is the main function for the model: S-SS-MTr.

- `SC-SS-MTr_main.py` is the main function for the model: SC-SS-MTr.
