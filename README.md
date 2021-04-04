## Introduction
*Transfer-Learn* is an open-source and well-documented library for Transfer Learning. It is based on pure PyTorch with high performance and friendly API. Our code is pythonic, and the design is consistent with torchvision. You can easily develop new algorithms, or readily apply existing algorithms.

On July 24th, 2020, we released the v0.1 (preview version), the first sub-library is for Domain Adaptation (DALIB). The currently supported algorithms include:

- [Domain Adversarial Neural Network 
(DANN)](https://arxiv.org/abs/1505.07818)
- [Deep Adaptation Network (DAN)](https://arxiv.org/abs/1502.02791)
- [Joint Adaptation Network (JAN)](https://arxiv.org/abs/1605.06636)
- [Conditional Domain Adversarial Network 
(CDAN)](https://arxiv.org/abs/1705.10667)
- [Maximum Classifier Discrepancy (MCD)](https://arxiv.org/abs/1712.02560)
- [Margin Disparity Discrepancy (MDD)](https://arxiv.org/abs/1904.05801)
- Regression DA （including Source Only, DD)
- Unsupervised DA (including MCC, AFN)
- Partial DA (DANN, PADA, IWAN)
- Open Set DA (DANN, OSBP)
- Segmentation DA (ADVENT, FDA, CycleGAN, Cycada)
- Keypoint Detection DA (RegDA)

We are planning to add
- Segmentation DA (Self-training methods)
- Finetune Library (ftlib)
- Object Detection DA

The performance of these algorithms were fairly evaluated in this [benchmark](http://microhhh.com/dalib/index.html).

## Installation

For flexible use and modification, please git clone the library.

## Documentation
You can find the tutorial and API documentation on the website: [Documentation (please open in Firefox or Safari)](http://170.106.108.162/index.html). Note that this link is only for temporary use. You can also build the doc by yourself following the instructions in http://170.106.108.162/get_started/faq.html.

Also, we have examples in the directory `examples`. A typical usage is 
```shell script
# Train a DANN on Office-31 Amazon -> Webcam task using ResNet 50.
# Assume you have put the datasets under the path `data/office-31`, 
# or you are glad to download the datasets automatically from the Internet to this path
python examples/dann.py data/office31 -d Office31 -s A -t W -a resnet50  --epochs 20
```

In the directory `examples`, you can find all the necessary running scripts to reproduce the benchmarks with specified hyper-parameters.

## Contributing
We appreciate all contributions. If you are planning to contribute back bug-fixes, please do so without any further discussion. If you plan to contribute new features, utility functions or extensions, please first open an issue and discuss the feature with us. 

## Disclaimer on Datasets

This is a utility library that downloads and prepares public datasets. We do not host or distribute these datasets, vouch for their quality or fairness, or claim that you have licenses to use the dataset. It is your responsibility to determine whether you have permission to use the dataset under the dataset's license.

If you're a dataset owner and wish to update any part of it (description, citation, etc.), or do not want your dataset to be included in this library, please get in touch through a GitHub issue. Thanks for your contribution to the ML community!


## Contact
If you have any problem with our code or have some suggestions, including the future feature, feel free to contact 
- Junguang Jiang (JiangJunguang1123@outlook.com)
- Bo Fu (fb1121@vip.qq.com)
- Mingsheng Long (longmingsheng@gmail.com)

or describe it in Issues.

For Q&A in Chinese, you can choose to ask questions here before sending an email. [迁移学习算法库答疑专区](https://zhuanlan.zhihu.com/p/248104070)

## Citation

If you use this toolbox or benchmark in your research, please cite this project. 

```latex
@misc{dalib,
  author = {Junguang Jiang, Bo Fu, Mingsheng Long},
  title = {Transfer-Learning-library},
  year = {2020},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/thuml/Transfer-Learning-Library}},
}
```

## Acknowledgment

We would like to thank School of Software, Tsinghua University and The National Engineering Laboratory for Big Data Software for providing such an excellent ML research platform.

