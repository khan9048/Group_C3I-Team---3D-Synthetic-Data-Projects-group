## Group_C3I-Team---3D-Synthetic-Data-Projects-group
* [Modeling of the Synthetic Dataset: Pixel-accurate facial depth generation process](#general-info)
* [Evaluating State-of-Art models for Single Image Depth Estimation](#technologies)
* [An Encoder-decoder based Facial Depth Estimation Model](#setup)
* [Hybrid Loss Function](#setup1)

## Single Frame Image Facial Depth Estimation
This is the project page for our research:<br/>

An Efficient Encoder-Decoder Model for Portrait Depth Estimation
from Single Images trained on Pixel-Accurate Synthetic Data

High-Accuracy Facial Depth Models derived from 3D Synthetic Data<br/>
https://ieeexplore.ieee.org/document/9180166<br/>

Methodology for Building Synthetic Datasets with Virtual Humans<br/>
https://ieeexplore.ieee.org/abstract/document/9180188<br/>

Learning 3D Head Pose From Synthetic Data: A Semi-Supervised Approach<br/>
https://ieeexplore.ieee.org/abstract/document/9369299<br/>

Accurate 2D Facial Depth Models Derived from a 3D Synthetic Dataset
https://ieeexplore.ieee.org/abstract/document/9427595<br/>





We will also update latest progress and available sources to this repository~ 
	
## Note
This repository contains PyTorch implementations of FaceDepth, UNet-Simple, BTS, DenseDepth.

## Generation Process of the Dataset
![data_method](https://user-images.githubusercontent.com/49758542/120590876-1fc03b00-c433-11eb-825f-2bd3ec8bc538.png)

## Setup & Requirements
To run this project, install it locally using pip install...:

```
$ pip install keras, Pillow, matplotlib, opencv-python, scikit-image, sklearn, pathlib, pandas, -U efficientnet,
$ pip install https://www.github.com/keras-team/keras-contrib.git, torch, torchvision
```

```
$ Python >= 3.6
Pytorch >= 1.6.0
Ubuntu 16.04
CUDA 9.2
cuDNN (if CUDA available)
```
## Pretrained model

download the pre-trained model and keep in the FaceDepth directory:

https://nuigalwayie-my.sharepoint.com/:u:/g/personal/f_khan4_nuigalway_ie/EepkuVajAhdIjZoQm5Weyx4BjXcEZy-uw5OWxxMXq1WJPA?e=rv3aSY

## Prepare Dataset for training & Testing 

We prepared the dataset for training and testing<br/>
contact me on the following email: f.khan4@nuigalway.ie for the complete dataset, I will provide the download link <br/>

#### Random sample frames with high-resolutions RGB images and their corresponding ground truth depth with differentvariations<br/>
![data_mix](https://user-images.githubusercontent.com/49758542/106769813-49a85300-6635-11eb-9b73-dd9935f8989d.png)

#### Samples from the generated synthetic data with different variation of head pose
![da](https://user-images.githubusercontent.com/49758542/106660977-9ab63980-6598-11eb-8754-3235cfd43bf3.png)

## Live Demo
We attach live demo implementation for Pytorch. \
Note change the model check point name if different 
```
$ cd FaceDepth
$ python live_demo.py
```
## Testing
First make sure that you have some images (RGB and depth) or you can use our test images: (rgb_syn_test) and (gt_syn_test).
```shell
$ cd FaceDepth
$ make a folder and keep your RGB images in that  
$ make a folder and keep your gt depth images in that
$ Change the path in the Facedepth_test.py
$ Name a folder that you want to save the predicted results (images)  
```
Once the preparation steps completed, you can test using following commands.
```
$ cd FaceDepth
$ python Facedepth_test.py
```
![image](https://user-images.githubusercontent.com/49758542/120592291-80e90e00-c435-11eb-832e-45b55b014336.png)

## Training
Once the dataset download process completed, please make sure unzip all the data into a new folder and follow the following steps:
```shell
$ cd FaceDepth
$ Download the .csv or .txt files
$ Change the paths in the train.py  
```
Once the preparation steps completed, you can train using following commands.
```
$ cd FaceDepth
$ python train.py --batch_size 4 --epochs 25 
```
#### Training BTS and DenseDepth methods for our synthetic facial depth dataset.
We referred to BTS and DenseDepth:

$ https://github.com/cogaplex-bts/bts

$ https://github.com/ialhashim/DenseDepth

## Results 
![image](https://user-images.githubusercontent.com/49758542/120593394-55672300-c437-11eb-8368-29078c44c38c.png)

Properties of the studied methods
![image](https://user-images.githubusercontent.com/49758542/120593446-6fa10100-c437-11eb-928e-a0f38f7c4a32.png)

Qualitative results of a facial monocular depth estimation methods
![image](https://user-images.githubusercontent.com/49758542/120593540-919a8380-c437-11eb-8bdb-1498b4472795.png)

![rrrr](https://user-images.githubusercontent.com/49758542/120594025-34530200-c438-11eb-920a-4f7c8640b57f.png)




# Citation
If you find the code, models, or data useful, please cite these paper:<br/>
F. Khan, S. Basak, H. Javidnia, M. Schukat and P. Corcoran, "High-Accuracy Facial Depth Models derived from 3D Synthetic Data," 2020 31st Irish Signals and Systems Conference (ISSC), Letterkenny, Ireland, 2020, pp. 1-5, doi: 10.1109/ISSC49989.2020.9180166.<br/>

S. Basak, H. Javidnia, F. Khan, R. McDonnell and M. Schukat, "Methodology for Building Synthetic Datasets with Virtual Humans," 2020 31st Irish Signals and Systems Conference (ISSC), Letterkenny, Ireland, 2020, pp. 1-6, doi: 10.1109/ISSC49989.2020.9180188.<br/>



  
  ## Citation
If you find this work useful for your research, please consider citing our paper:
```
@INPROCEEDINGS{9427595,
  author={Khan, Faisal and Basak, Shubhajit and Corcoran, Peter},
  booktitle={2021 IEEE International Conference on Consumer Electronics (ICCE)}, 
  title={Accurate 2D Facial Depth Models Derived from a 3D Synthetic Dataset}, 
  year={2021},
  volume={},
  number={},
  pages={1-6},
  doi={10.1109/ICCE50685.2021.9427595}}
  
  @INPROCEEDINGS{9180166,
  author={Khan, Faisal and Basak, Shubhajit and Javidnia, Hossein and Schukat, Michael and Corcoran, Peter},
  booktitle={2020 31st Irish Signals and Systems Conference (ISSC)}, 
  title={High-Accuracy Facial Depth Models derived from 3D Synthetic Data}, 
  year={2020},
  volume={},
  number={},
  pages={1-5},
  doi={10.1109/ISSC49989.2020.9180166}}
  
  @INPROCEEDINGS{9180188,  author={Basak, Shubhajit and Javidnia, Hossein and Khan, Faisal and McDonnell, Rachel and Schukat, Michael},  booktitle={2020 31st Irish Signals and Systems Conference (ISSC)},   title={Methodology for Building Synthetic Datasets with Virtual Humans},   year={2020},  volume={},  number={},  pages={1-6},  doi={10.1109/ISSC49989.2020.9180188}}
  
  @ARTICLE{9369299,  author={Basak, Shubhajit and Corcoran, Peter and Khan, Faisal and Mcdonnell, Rachel and Schukat, Michael},  journal={IEEE Access},   title={Learning 3D Head Pose From Synthetic Data: A Semi-Supervised Approach},   year={2021},  volume={9},  number={},  pages={37557-37573},  doi={10.1109/ACCESS.2021.3063884}}
```



