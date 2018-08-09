# Semantic Tissue Segmentation

Disclaimer: Unfortunately dataset canot be shared publicly due to NDA.

Project was done on small 27+8 microscopy images with a goal of classifying whether each pixel on the image is a human tissue or not.
Main challenges were mainly related to sample size, unbalanced classes. two different augmentations pipelines were used with two different models.

## Models.

* **TernausNet** ([arXiv paper](https://arxiv.org/abs/1801.05746)) - U-Net with VGG11 Encoder Pre-Trained on ImageNet for Image Segmentation implemented from [github repository](https://github.com/ternaus/TernausNet)



###### Introduction

TernausNet is a modification of the celebrated UNet architecture that is widely used for binary Image Segmentation.

![UNet11](https://habrastorage.org/webt/hu/ji/ir/hujiirvpgpf7eswq88h_x7ahliw.png)

(Network architecure)

![loss_curve](https://habrastorage.org/webt/no/up/xq/noupxqqk_ivqwv3e7btyxtemt0m.png)

Pre-trained encoder speeds up convergence even on the datasets with a different semantic features. Above curve shows validation Jaccard Index (IOU) as a function of epochs for [Aerial Imagery](https://project.inria.fr/aerialimagelabeling/)


* **Vanilla U-Net**

###### Introduction

The architecture was inspired by [arxiv paper](http://lmb.informatik.uni-freiburg.de/people/ronneber/u-net/) and [github repository](https://github.com/zhixuhao/unet)

![img/u-net-architecture.png](https://lmb.informatik.uni-freiburg.de/people/ronneber/u-net/u-net-architecture.png)
