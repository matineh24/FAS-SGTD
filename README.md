# FAS-SGTD

---

## Introduction

Main codes of [**CVPR2020 paper "Deep Spatial Gradient and Temporal Depth Learning for Face Anti-spoofing"**  ](https://arxiv.org/abs/2003.08061)

## Prerequisite

* Python 3.6 (numpy, skimage, scipy)

* TensorFlow >= 1.4

* opencv2

* Pillow (PIL)

* easydict

## Test

To test this project, first follow the instructions in [PRNet](https://github.com/matineh24/PRNet-Depth-Generation) project to generate the proper data.

We provide an example for Protocol 1 of OULU-NPU. You can download the models at [BaiduDrive](https://pan.baidu.com/s/1sVdctfWDoUFsrXOjxr6wJw)(pwd: luik) or  [GoogleDrive](https://drive.google.com/drive/folders/1CW1sXkLZRUmoDjg8LpQJ8-93Baz2TB2B?usp=sharing) and put them into `fas_sgtd_multi_frame/model_save/`. Also get the data and modify it with PRNet project and put it into `fas_sgtd_multi_frame/data/` and add the name of the folders in [FLAGS.py](https://github.com/matineh24/FAS-SGTD/blob/9dfefb133ef20b96f9b3141696824916ccbd09b7/fas_sgtd_multi_frame/FLAGS.py#L11) based on your dev and test folders. Then you could run test.py file. 

If you want to use batch to run, remove [this line](https://github.com/matineh24/FAS-SGTD/blob/9dfefb133ef20b96f9b3141696824916ccbd09b7/fas_sgtd_multi_frame/generate_network.py#L15) and run:

> cd fas_sgtd_multi_frame && bash test.sh


## Data

You can access the self_created dataset [here](https://drive.google.com/file/d/1ktju-N4sNut-4pUCgaj-S9Th5D7TbCYB/view?usp=sharing). 

## Evaluation

Evaluation on the modified original data can be found [here](https://github.com/matineh24/FAS-SGTD/blob/cca9608b895e95a3f8b52bd9efaae253d138e695/fas_sgtd_multi_frame/scores/norm_fusion_att_0.40_0.80/Protocol_1/eval.txt#L1) and evaluation on the new data can be found [here](https://github.com/matineh24/FAS-SGTD/blob/cca9608b895e95a3f8b52bd9efaae253d138e695/fas_sgtd_multi_frame/scores/norm_fusion_att_0.40_0.80/Protocol_1/eval.txt#L2). 

According to this [line](https://github.com/matineh24/FAS-SGTD/blob/cca9608b895e95a3f8b52bd9efaae253d138e695/fas_sgtd_multi_frame/util/performances.py#L43) APCER, BPCER, and ACER are columns 4,5,6 respectively.

When you test on a new data a row would be added to this text file.

## Extra

[This file](https://github.com/matineh24/FAS-SGTD/blob/master/download_from_aws.ipynb) was used to download only dev and test files of protocol 1 of OULU-NPU dataset. This has been run on AWS and the path of S3 bucket is filtered due to privacy reasons. 





## License

Code: under MIT license.

It is just for **research purpose**, and commercial use is not allowed

## Citation

If you use this code, please consider citing:

 >@inproceedings{wang2020deep,  
 >&nbsp;&nbsp;&nbsp;&nbsp;title={Deep Spatial Gradient and Temporal Depth Learning for Face Anti-spoofing},      
 >&nbsp;&nbsp;&nbsp;&nbsp;author={Wang, Zezheng and Yu, Zitong and Zhao, Chenxu and Zhu, Xiangyu and Qin, Yunxiao and Zhou, Qiusheng and Zhou, Feng and Lei, Zhen},  
 >&nbsp;&nbsp;&nbsp;&nbsp;booktitle= {CVPR},  
 >&nbsp;&nbsp;&nbsp;&nbsp;year = {2020}  
 >}  

 >@inproceedings{yu2020searching,  
 >&nbsp;&nbsp;&nbsp;&nbsp;title={Searching Central Difference Convolutional Networks for Face Anti-Spoofing},      
 >&nbsp;&nbsp;&nbsp;&nbsp;author={Yu, Zitong and Zhao, Chenxu and Wang, Zezheng and Qin, Yunxiao and Su, Zhuo and Li, Xiaobai and Zhou, Feng and Zhao, Guoying},  
 >&nbsp;&nbsp;&nbsp;&nbsp;booktitle= {CVPR},  
 >&nbsp;&nbsp;&nbsp;&nbsp;year = {2020}  
 >}  


 >@inproceedings{qin2019learning,  
 >&nbsp;&nbsp;&nbsp;&nbsp;title={Learning Meta Model for Zero-and Few-shot Face Anti-spoofing},      
 >&nbsp;&nbsp;&nbsp;&nbsp;author={Qin, Yunxiao and Zhao, Chenxu and Zhu, Xiangyu and Wang, Zezheng and Yu, Zitong and Fu, Tianyu and Zhou, Feng and Shi, Jingping and Lei, Zhen},  
 >&nbsp;&nbsp;&nbsp;&nbsp;booktitle= {AAAI},  
 >&nbsp;&nbsp;&nbsp;&nbsp;year = {2020}  
 >}  
