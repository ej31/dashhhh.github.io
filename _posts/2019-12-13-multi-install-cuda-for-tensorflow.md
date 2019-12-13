---
layout: post
title: Tensorflow + Cuda (multi install)
date: 2019-12-13
category: Tensorflow
tags: tensorflow cuda
---

Tensorflow - 'Cuda Multi install'
=
### Cuda Multi version Install
Tensorflow 버전에 따라 Cuda를 별도로 설정해 주어야 한다
Cuda는 한개만 설치 할 수 있는 개념이 라고 알고 있었으나, 자세히 보니 여러 버전을 동시에 설치 할 수 있는 거였다.

Cuda를 여러개 설치 할 때 몇 가지 실수 하는 점은 다음과 같다
- Tensorflow 버전마다 맞는 Cuda 버전이 따로 있다.
- 해당 내용 상세는 아래 링크에서 확인 할 수 있다.
  - [Tensorflow Version Dependency Index](https://tensorflow.org/install/source#tested_build_configurations)
  - ![image](https://user-images.githubusercontent.com/25720120/70801286-d8369100-1df1-11ea-8d11-ca5c149b3da9.png)
  - ![image](https://user-images.githubusercontent.com/25720120/70801349-01572180-1df2-11ea-872c-c5cfb265874b.png)
  - 위 Index는 절대적인 기준은 아니지만 버전이 안맞으면 `libcublas`와 같은 library 호출을 실패한다 (해당 호출은 `/usr/local/cuda-x.x` 를 바라본다. 정확하게는 `LD_LIBRARY_PATH`를 쳐다보고 있다.)
 
CUDA 버전별로 손 쉽게 설치하는 방법
나중에 올려야겠네..


