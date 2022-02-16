# HunanMultimodalDataset
A multimodal (i.e., Sentinel-2, Sentinel-1, and SRTM) remote sensing dataset of year 2017 in Hunan, China.

# Title
DKDFN: Domain Knowledge-Guided Deep Collaborative Fusion Network for Multimodal Remote Sensing Yearly Composite Land Cover Classification

# Abstract
Land use and land cover maps provide fundamental information that has been used in different types of studies, ranging from public health to carbon cycling. However, the existing remote sensing image classification methods thus far suffer from the insufficient usage of multiple modalities, underconsideration of prior domain knowledge, and poor performance on minority classes. To alleviate these problems, we propose a novel domain knowledge-guided deep collaborative fusion network (DKDFN) with performance boosting for minority categories for land cover classification. More specifically, the DKDFN adopts a multihead encoder and a multibranch decoder structure. The architecture of the encoder probablizes sufficient mining of complementary information from multiple modalities, which are Sentinel-2, Sentinel-1, and SRTM Digital Elevation Data (SRTM) in our case. The multibranch decoder enables land cover classification in a multitask learning setup, performing semantic segmentation and reconstructing multimodal remote sensing indices, which are selected as representatives of domain knowledge. This design incorporates domain knowledge in an effective end-to-end manner. The training stage of our DKDFN is supervised by our proposed asymmetry loss function (ALF), which boosts performance on nearly all categories, especially the categories with a low frequency of occurrence. Ablation studies of the network suggest that our design logic is worth testing in any network with an encoder-decoder structure. The study is conducted in Hunan, China and is verified using a self-labeled multimodal dataset. The comparative experiments between DKDFN and 6 state-of-the-art models (U-Net, SegNet, PSPNet, DeepLab, HRNet, MP-ResNet) testify to the superiority of our proposed method and suggest its potential to be applied more widely to map land cover in other geographical areas given the availability of Sentinel-2, Sentinel-1, and SRTM data. The collected dataset will be made publicly available along with this paper.


# Dataset Description

