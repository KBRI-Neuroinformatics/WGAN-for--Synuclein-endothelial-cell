# WGAN-for--Synuclein-endothelial-cell
Code for paper "α-synuclein induces endothelial disruption mediated by NF-κB-regulated inflammatory responses".
\\<!--Please read our preprint at the following link:""-->
![WGAN_overveiw](https://user-images.githubusercontent.com/57948381/194007259-31720723-3108-4624-9a94-2b861db24a2a.PNG)

Abstract : Disruption of the blood–brain barrier (BBB) integrity is highly correlated with neurodegenerative disease progression. This study aimed to reveal the pathological role of α-synuclein (α-syn) on the integrity and function of the BBB. BBB integrity was severely compromised in in vivo and in vitro models. Generative adversarial networks (GANs) were applied for RNA sequencing of human brain endothelial cells (ECs) upon treatment with α-syn. α-syn could induce significant upregulation of pathways related to various immune responses. GAN analysis revealed that genes are governed by TNFα-associated signaling and nuclear factor-kappa B (NF-B)-associated responses. TNFα-associated signaling inhibition can preserve BBB integrity from α-syn’s pathological effect. Conversely, the pathological α-syn can induce harmful effects on the BBB mediated through TNFα-related inflammatory responses in brain ECs.
One -Sentence Summary: α-synuclein induces pathological damage to the brain via NF-κB-mediated inflammatory responses

## Dependencies 

This software was originally designed and run on a system running Ubuntu 18.04 with Python 3.3.6. For neural network model training and interpretation, we used a single Nvidia GeForce GTX 980 Ti GPU, though we anticipate that other GPUs will also work. Standard python software packages used: Tensorflow (1.3.0), Keras (2.0.4), numpy (1.17.3), pandas (0.24.1), scipy (1.3.1), scikit-learn (0.21.3), matplotlib (3.1.2), seaborn (0.9.0), h5py (2.9.0). We additionally used the following Python software packages available here: [IntegratedGradients](https://github.com/hiranumn/IntegratedGradients), and [GSEApy](https://pypi.org/project/gseapy/). 

## Acknowledgments  

This work supported by KBRI basic research program through KBRI funded by the Ministry of Science, ICT & Future Planning (grant numbers: 22-BR-02-04 to M.C. and D.G.K., and 22-BR-04-01 to D.G.K.).
