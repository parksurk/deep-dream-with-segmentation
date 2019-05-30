Image Segmentation + Style Transfer + Deep Dream = 꿈속의 꿈
================================
Modulabs DLC - CreativedAI VideoLab 한정협, 김준화, 박석
-------------------------------------------

---


### Project Details

For this project, we are inspired from 'Deep Dream' by Alexander Mordvintsev https://github.com/tensorflow/tensorflow/tree/master/tensorflow/examples/tutorials/deepdream

# 1. 어떤 것을 하고 싶은지? 주제

- Image Segmentation + Style Transfer + Deep Dream = 꿈속의 꿈
- 사람과 배경이 있는 이미지에서 배경에만 Style Transfer 와 Deep Dream 을 적용하여, 사람 영역에 괴기스럽게 변하는 단점을 보완하여 좀 더 자연스러운 이미지를 Generation하고자 함.

# 2. 어떻게 만들 것인지 : 어떤 알고리즘을 사용하고 싶고, 어떤 데이터셋을 이용할 것인가?

1. Image Segmentation (DeepLab V3+) : [https://github.com/bonlime/keras-deeplab-v3-plus](https://github.com/bonlime/keras-deeplab-v3-plus)
2. Style Transfer (Neural Transfer using PyTorch) : [https://pytorch.org/tutorials/advanced/neural_style_tutorial.html](https://pytorch.org/tutorials/advanced/neural_style_tutorial.html)
3. Deep Dream (GoogLeNet) :  [https://github.com/tensorflow/tensorflow/tree/master/tensorflow/examples/tutorials/deepdream](https://github.com/tensorflow/tensorflow/tree/master/tensorflow/examples/tutorials/deepdream)

# 3. 그렇게 생각하게 된 이유는?

- 원본이미지 → "Image Segmentation" → "사람 영역 One-Hot Vector", "배경 영역 One-Hot Vector"
- 원본이미지 → "Style Transfer" → 특정 Style이 적용된 이미지
- 특정 Style이 적용된 이미지 → "Deep Dream" → 몽환적 분위기 이미지
- 몽환적 분위기 이미지 → "Additional Image Processing" → 몽환적 분위기 이미지 + 원본 사람 영역이 치환된 좀 더 자연스러운 이미지

# 4. 사용할 데이터셋 : 작업의 특징을 고려한 데이터셋

1. Image Segmentation (DeepLab V3+) : COCO & JFT
2. Style Transfer (Neural Transfer using PyTorch) : vgg19
3. Deep Dream (GoogLeNet) : Imagenet
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
