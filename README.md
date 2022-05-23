# HunanMultimodalDataset
A multimodal (i.e., Sentinel-2, Sentinel-1, and SRTM) remote sensing dataset of year 2017 in Hunan, China.

# Dataset Link
https://drive.google.com/file/d/1m3wYiQolm2YEmpzH6cGQZ4wWw_EdFAdN/view?usp=sharing

# Title
DKDFN: Domain Knowledge-Guided Deep Collaborative Fusion Network for Multimodal Remote Sensing Yearly Composite Land Cover Classification

# Abstract
Land use and land cover maps provide fundamental information that has been used in different types of studies, ranging from public health to carbon cycling. However, the existing remote sensing image classification methods thus far suffer from the insufficient usage of multiple modalities, underconsideration of prior domain knowledge, and poor performance on minority classes. To alleviate these problems, we propose a novel domain knowledge-guided deep collaborative fusion network (DKDFN) with performance boosting for minority categories for land cover classification. More specifically, the DKDFN adopts a multihead encoder and a multibranch decoder structure. The architecture of the encoder probablizes sufficient mining of complementary information from multiple modalities, which are Sentinel-2, Sentinel-1, and SRTM Digital Elevation Data (SRTM) in our case. The multibranch decoder enables land cover classification in a multitask learning setup, performing semantic segmentation and reconstructing multimodal remote sensing indices, which are selected as representatives of domain knowledge. This design incorporates domain knowledge in an effective end-to-end manner. The training stage of our DKDFN is supervised by our proposed asymmetry loss function (ALF), which boosts performance on nearly all categories, especially the categories with a low frequency of occurrence. Ablation studies of the network suggest that our design logic is worth testing in any network with an encoder-decoder structure. The study is conducted in Hunan, China and is verified using a self-labeled multimodal dataset. The comparative experiments between DKDFN and 6 state-of-the-art models (U-Net, SegNet, PSPNet, DeepLab, HRNet, MP-ResNet) testify to the superiority of our proposed method and suggest its potential to be applied more widely to map land cover in other geographical areas given the availability of Sentinel-2, Sentinel-1, and SRTM data. The collected dataset will be made publicly available along with this paper.


# Dataset Description
This dataset contains 400 256*256 images for training, 50 for validation and test. Note that the training set contains TRI, which is computed from SRTM by GDAL, and can be used for knowledge reconstruction.

# Dataset Process
Potential users of this dataset should utilize the following code to preprocess the label.

```
from skimage import io

igbp2hunan = np.array([255, 0, 1, 2, 1, 3, 4, 6, 6, 5, 6, 7, 255])

def load_lc(path):
    lc = io.imread(path)
    lc[lc == 255] = 12
    lc = igbp2hunan[lc]
    return lc
```

Note that after processing, the label will be in 0-6, where 0 stands for cropland, 1 stands for forest, 2 stands for grassland, 3 stands for wetland, 4 stands for water, 5 stands for bare land, and 6 stands for others.
