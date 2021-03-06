# MobileNet-MXNet

### Introduction

This is a MXNet implementation of Google's MobileNets. For details, please read the original paper:
- [MobileNets: Efficient Convolutional Neural Networks for Mobile Vision Applications](https://arxiv.org/abs/1704.04861)


### Pretrained Models on ImageNet

A pretrained MobileNet model on ImageNet is provided and you can use score.py to reproduce the accuracy in ImageNet 2012 val dataset.

The top-1/5 accuracy rates by using single center crop (crop size: 224x224, image size: 256xN):

Network|Top-1|Top-5|
:---:|:---:|:---:|
MobileNet| 71.24| 90.15|


### Notes

- RGB mean values **[123.68,116.78,103.94]** are subtracted
- **scale: 0.017** is used as std values for image preprocessing
- I use ChannelwiseConvolution layer from [paper](https://github.com/cypw/CRU-Net)
- This model is converted from [MobileNet-Caffe](https://github.com/shicai/MobileNet-Caffe)
- If you like it, consider giving me a star.
- I've finished a fast Depthwise mxnet operator! Now the infer time of mobilenet is 0.002s/image (batch-size=1, TITANX). Acc is 0.708. (The code will come soon!)
