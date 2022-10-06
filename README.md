# WGAN for α-Synuclein endothelial cell
Code for paper "α-synuclein induces endothelial disruption mediated by NF-κB-regulated inflammatory responses".

<!--Please read our preprint at the following link:""-->
![WGAN_overveiw](https://user-images.githubusercontent.com/57948381/194007259-31720723-3108-4624-9a94-2b861db24a2a.PNG)

Abstract : Disruption of the blood–brain barrier (BBB) integrity is highly correlated with neurodegenerative disease progression. This study aimed to reveal the pathological role of α-synuclein (α-syn) on the integrity and function of the BBB. BBB integrity was severely compromised in in vivo and in vitro models. Generative adversarial networks (GANs) were applied for RNA sequencing of human brain endothelial cells (ECs) upon treatment with α-syn. α-syn could induce significant upregulation of pathways related to various immune responses. GAN analysis revealed that genes are governed by TNFα-associated signaling and nuclear factor-kappa B (NF-B)-associated responses. TNFα-associated signaling inhibition can preserve BBB integrity from α-syn’s pathological effect. Conversely, the pathological α-syn can induce harmful effects on the BBB mediated through TNFα-related inflammatory responses in brain ECs.

One -Sentence Summary: α-synuclein induces pathological damage to the brain via NF-κB-mediated inflammatory responses

## Software installation and training WGAN 

### [Prerequisites]
* __Create virtual environment__  

          virtualenv WGAN_endo --python=python3.7
          
          source WGAN_endo/bin/activate  

* __Install packages__  
    
          pip install -r requirements.txt

### [Dependencies]

This software was originally designed and run on a system running Ubuntu 18.04 with Python 3.3.9. For neural network model training and interpolation, we used a single NVIDIA® Quadro RTX 5000 (16GB GDDR6) GPU, though we anticipate that other GPUs will also work. Standard python software packages used: Tensorflow (2.2.0), numpy (1.19.5), pandas (1.1.5), scipy (1.4.1), scikit-learn (0.24.2), matplotlib (3.2.2), seaborn (0.11.1). 

### [Usage]
__Train and Analysis using <수정 필요>WGAN_for_toupathy.ipynb__
  * __Network architecture and hyperparameters__    
    * We adopted the advanced Wasserstein GAN with gradient penalty, which consists of two networks, generator and discriminator, and contains several advanced features for learning (16, 17). We implemented the two networks composed of fully connected layers (FC) and leaky rectified linear unit (ReLU) activation function. We set the number of hidden layer units for the generator and discriminator to 400 and 240, respectively. Thus, the architecture of the generator and discriminator were input FC (100)—leaky ReLU—hidden FC (400)—leaky ReLU—hidden FC (400)—leaky ReLU—output FC (2,254); and input FC (2,254)—leaky ReLU—hidden FC (240)—leaky ReLU—hidden FC (240)—leaky ReLU—output FC (1), respectively. In addition, we set the initial random weight parameters in the generator within the range [-0.3, 0.3] and generated random variables in the latent space determined by the distribution of the rescaled regularized logarithmic profile data. The weights were updated by learning based on the loss of the Wasserstein GAN with gradient penalty (gradient penalty = 10) with Adam optimizer (initial learning rate = 1e-5 and cosine decay restarts schedule) for 200,000 epochs with a minibatch size of 64. We evaluated the generator output performance at multiple checkpoints using t-distributed stochastic neighbor embedding (t-SNE) (20) and correlation between real and generated samples.<br/>

## Acknowledgments  

This work supported by KBRI basic research program through KBRI funded by the Ministry of Science, ICT & Future Planning (grant numbers: 22-BR-02-04 to M.C. and D.G.K., and 22-BR-04-01 to D.G.K.).
