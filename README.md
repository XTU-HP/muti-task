# NAFSL
Few-shot learning (FSL) through training few labelled sample in source domain and fine-tuning in target domain has gotten increasing attention since it shows robust classification capability with few labeled samples of hyperspectral images (HSI). However, in current FSL for HSI classification (HSIC), the number of classes trained in the source-domain feature extractor is contingent upon the number of task classes in the target domain, which restricts the availability and the generalization of the transferable knowledge learned in the source domain. At the same time, due to the diverse spatial resolutions in multi-source domain, the most existing multi-scale feature extractors fuse features by summing the pixel-wise feature between layers, which potentially generate a significant amount of redundant information, leading to the blurred details and inaccurate classification. To address the issues, we propose a non-aligned multi-scale FSL method for HSI classification. Firstly, a non-aligned multi-source FSL framework is established, which comprises multiple independent sources providing rich transferable knowledge for HSI classification, and each source trains respective classes, eliminating the need for aligning the number of classes with the target's.  Secondly, a multi-scale feature differential network is constructed to obtain feature differences between neighboring layers through a feature difference unit (FDU),  which provides detailed pixel's differential information and facilitates to exploit feature variations at different scales for the feature extractor. Furthermore, to alleviate the training burden on the network resulting from the non-aligned training strategy, a hybrid loss function is devised to augment the inter-class distance while reducing the intra-class distance, thereby promoting the classification. Experiments conducted on three public hyperspectral datasets demonstrate that the model of the present method outperforms existing FSL methods for Hyperspectral image classification.

Requirements
Python = 3.6.12 Pytorch = 1.0.1 sklearn = 0.0 numpy = 1.19.2 tensorflow = 1.13.1

dataset
Take HCFSL-NAS method on the IP dataset as an example: You can also download the hyperspectral datasets from the following link. Link: https://pan.baidu.com/s/1atfmqJJh134dxAeAF8KJaQ Extract code: 3vcy An example dataset folder has the following structure:

datasets
├── PU
│   ├── indian_pines.mat
│   ├── indian_pines_corrected.mat
│   ├── indian_pines_gt.mat
└── Chikusei_imdb_128.pickle
└── IP


## Usage:
Take HFSL method on the PU dataset as an example: 
1. Download the required data set and move to folder`./datasets`.
2. To run the file: HSI_search.py
3. To run the file: HCFSL_NAS_IP.py. 
