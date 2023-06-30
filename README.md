# DepthEstimationInFoy

## Table of Contents
- [Background](#background)
- [Install](#install)
- [Usage](#usage)
- [Quantitative Result](#quantitative-result)
- [Contributing](#contributing)
- [License](#license)

## Background 
This is our work for 2022, about the self-supervised monocular depth estimation in foggy scenes:

> **Self-supervised monocular depth estimation in fog**
>
>Bo Tao<sup>**†**</sup>, Jiaxin Hu<sup>**†**</sup>, Du Jiang, Gongfa Li, Baojia Chen, Xinbo Qian
>
> <sup>**†**</sup>These authors contributed equally to this work.
> 
> [Optical Engineering 2022](https://doi.org/10.1117/1.OE.62.3.031208)
> 
<p align="center">
  <img src="https://github.com/Hjxin02AIsharing-Wust/DepthEstimationInFoy/blob/f390f8785f82dbe00a14efad2010c025e29bf123/pictures/Image%20of%20the%20qualitative%20result.png" alt="example input output gif" width="500" />
</p>

![image](https://github.com/Hjxin02AIsharing-Wust/DepthEstimationInFoy/blob/f390f8785f82dbe00a14efad2010c025e29bf123/pictures/Image%20of%20the%20network%20framework.png)


We have provided an implementation based on Pytorch here. **Please note that it is only used to communicate with scholars in this field and record our own learning results**.

If you find our work useful in your research, please consider citing our paper:
```
@article{DepthEstimationInFoy,
  title     = {Self-supervised monocular depth estimation in fog},
  author    = {Bo Tao, Jiaxin Hu, Du Jiang, Gongfa Li, Baojia Chen, Xinbo Qian},
  booktitle = {Optical Engineering (Opt.Eng)},
  month = {December},
year = {2022}
}
```

## Install
Please install the latest [Anaconda](https://www.anaconda.com/download/) distribution, you can refer to the following configuration to build your environment:
```shell
conda create -n DepthEstimationInFoy python=3.6
conda install pytorch=0.4.1 torchvision=0.2.1 -c pytorch
pip install tensorboardX==1.4
pip install opencv-python
pip install ipython
pip install scikit-image
```
We ran our experiments with PyTorch 0.4.1, CUDA 10.1, Python 3.6.6 and Windows.
We have successfully trained models with PyTorch. Adam optimizer is used to train 20 epochs on an RTX 1080Ti GPU. The batch size is set to 6. And learning rate is initially set to le − 4, and after 5
epochs, it is set to 1e − 5. Seven metrics, Abs-Rel, Sq-Rel, RMSE, RMSE-log, δ1, δ2, and δ3, were used for test.

## Usage

### - Data

We used the left image of the front stereo camera in the sequence taken from 2011-09 in the [KITTI dataset](http://www.cvlibs.net/datasets/kitti/raw_data.php) as the clear image set. For the synthetic
fog images set, 29,998 clear-synthetic fog map image pairs were generated by referring to [paper](https://doi.org/10.1007/s11263-018-1072-8).The real-world fog images are from the [Oxford RobotCar datasets](https://robotcar-dataset.robots.ox.ac.uk/).

We will release these datasets publicly soon. 

### - Model

We provide pre-trained models, you can download it here, and use your own datasets or the datasets provided by us to make better adjustments, which may achieve better results. 

You can also download the model weights that we have trained for testing. 



### - Prediction for a single image

### - Training

### - Evaluation

## Quantitative Result

## Contributing

## License






