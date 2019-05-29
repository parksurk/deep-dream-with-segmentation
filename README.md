Deep Dream with Image Segmentation
================================

Experiment Deep Dream using Image Segmentation
-------------------------------------------

---


### Project Details

For this project, we are inspired from 'Deep Dream' by Alexander Mordvintsev https://github.com/tensorflow/tensorflow/tree/master/tensorflow/examples/tutorials/deepdream

- Our Experiment Idea : Google Deep Dream 사례를 보면… ImageNet DataSet을 CNN으로 학습한 ‘Image Classification’  Pretrained Model 을 가져와 CNN의 특정 Feature Channel을 선택한 후 원본 이미지에 해당 Feature를 부각시켜 새로운 Image를 Generation 했습니다.
저희의 Idae는 Deep Dream 사례를 ‘Image Classification’  Pretained Model 이 아닌 CNN기반의 ‘Image Segmentation’ Pretrained Mdel을 가져와서 실험해서 좀 더 재밌는 결과를 얻는 것입니다.
- Image Segmentation reference(DeepLab V3+) : https://github.com/bonlime/keras-deeplab-v3-plus
- DeepLab V3+ Pretrained Medel 사용 사례 : https://medium.com/hyunjulie/2%ED%8E%B8-%EB%91%90-%EC%A0%91%EA%B7%BC%EC%9D%98-%EC%A0%91%EC%A0%90-deeplab-v3-ef7316d4209d

---

### Instructions

To setup our project environment to run the code in this repository, follow the instructions below.


1. Install Git
	-	Linux: https://www.atlassian.com/git/tutorials/install-git#linux
	- Mac: https://www.atlassian.com/git/tutorials/install-git#mac-os-x
	-	Windows: https://www.atlassian.com/git/tutorials/install-git#windows

2. Install Anaconda
	-	Linux: https://docs.anaconda.com/anaconda/install/linux/
	- Mac: https://docs.anaconda.com/anaconda/install/mac-os/
		- [Download for Mac](https://drive.google.com/file/d/1HVymmlUe5_wLMvNrEGxYwLNnya6vhNpz/view?usp=sharing)
	-	Windows: https://docs.anaconda.com/anaconda/install/windows/

3.	Clone this repository
	- [Reference #1 : Intorduction to Git for Data Science](https://www.datacamp.com/courses/introduction-to-git-for-data-science)
	- [Reference #2 : Git the simple guide](https://rogerdudler.github.io/git-guide/index.ko.html)

```
git clone https://github.com/parksurk/deep-dream-with-segmentation
```
4.	Create (and activate) a new environment with Python 3.6.
	-	Linux or Mac:
		```
		conda create --name deepdream python=3.6
		source activate deepdream
		```
	-	Windows:
		```
		conda create --name deepdream python=3.6
		activate deepdream
		```
5.	Install Python Scientific Libraries

```
pip install jupyter numpy tensorflow pillow keras matplotlib opencv-python
```

6. Install [RISE](https://github.com/damianavila/RISE) - Jupyter notebook slideshow library (Optional for Presenter)

```
conda install -c conda-forge rise
```

7.	Create an IPython kernel for the kaggle environment. (Skip if you done already)

```
pip install ipykernel
python -m ipykernel install --user --name deepdream --display-name "deepdream"
```

8.	Run Jupyter Notebook

```
jupyter notebook
```

9.	Click **.ipynb** on root directory

10.	Before running code in a notebook, change the kernel to match the 'deepdream' environment by using the drop-down Kernel menu.
