# Does Composed Image Retrieval Really Need Dedicately Designed Combination Tricks?

## Introduction

Composed image retrieval (CIR) ([Vo et al., 2018](https://arxiv.org/pdf/1812.07119)) is a multi-modal task which takes a reference image and a modification text as input to search for a specific target image in a database. Current research efforts focus on improving retrieval accuracy by effectively combining image and text features. The prevalent state-of-the-art methods typically employ one of two strategies: Late-Fusion ([Tian et al., 2025](https://www.researchgate.net/publication/390113383_CCIN_Compositional_Conflict_Identification_and_Neutralization_for_Composed_Image_Retrieval), [Chen et al., 2024](https://arxiv.org/pdf/2211.07394v5), [Li et al., 2025](https://ojs.aaai.org/index.php/AAAI/article/view/32541)) integrates separately encoded image and text features at a later stage of the network and Textual-Inversion ([Saito et al., 2023](https://arxiv.org/pdf/2302.03084), [Bai et al., 2024](https://arxiv.org/pdf/2310.05473)) maps the visual concent into the textual domain to create a single combined feature for the query. As pre-trained models like CLIP, BLIP and BLIP-2 (Q-Former) emerges, the capability of extracting feature and fusion feature improved too.

## Analysis of one representative method

SPRC ([Bai et al., 2024](https://arxiv.org/pdf/2310.05473)), selected as ICLR'24 spotlight demonstates that learning
an appropriate sentence-level prompt for the relative caption (SPRC) is sufficient
for achieving effective composed image retrieval. It first utilizes Q-Former to fuse reference image and modification text and then 