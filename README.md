# Greduation-Project

### 프로젝트 소개

- 팀 명
  - 7조
- 개발 계기
  - 행동인식을 통해 헬스케어부문에 다양하게 쓰인다.
  - OpenPose API를 사용해 여러 행동을 인식하여 분석
- 개발 Point
  - 영상 데이터 전처리, MLP, CNN, RCNN 3가지 방식의 데이터학습
- 기술 스택
  - C/C++
    : OpenPose API
  - Python
    : Jupyter Notebook으로 환경설정 및 학습
  - AI
    : MLP, CNN, RCNN



### 주요 기능

데이터 전처리
```
영상속 신체의 움직임을 25곳의 포인트를 잡아 데이터화 진행
한 포인트 별로 (x, y, score) 형태로 변환 이를 15 프레임 단위로 나눔
```

MLP
```
이미지 위의 포인트의 위치와 값을 학습하기 때문에 이미지에 약한 MLP의 문제를 보완하였고
Drop Out을 통해 많은 양의 계산들을 잊으며 학습을 진행하였다.

실험셋에서 90%이상 테스트셋에서 80% 이상의 정확도를 보였고 학습 데이터의 양이 충분하다면
그 이상의 정확도를 얻을 수 있을것으로 보인다.
```
CNN
```
원본 이미지자체로는 실험 환경에서는 잘 나오지만 테스트환경에서 성능이 엄청 떨이지게 된다.
때문에 이미지를 데이터화하고 이를 다시 이미지화하여 학습을 진행
의도했던 것보다 더 줄어든 데이터 때문에 학습결과가 높지 않았다. 
신체 포인트별로 각 프레임 마다 변화하는 위치 벡터값으로도 시도하였지만 결과는 비슷하였다.
```
RCNN
```
이미지를 정규하여 학습에 이용
조금 더 높은 학습 정확도를 보였지만 CNN에서 이미지 자체만으로 학습했던 결과와 비슷하였다.
뒷 배경에 대한 데이터를 걷어내고 RNN을 통해 학습 할 수 있다면 더 나은 결과를 얻을 수 있을것으로 생각된다.
```


### 프로젝트 결과

- [프로젝트 PPT](https://github.com/shampookim/Greduation-Project/blob/main/7%EC%A1%B0%20%EB%B0%9C%ED%91%9C_%EC%B5%9C%EC%A2%85.pdf)

### 프로젝트 실행영상
[![video-preview](https://img.youtube.com/vi/CT5dl_k9gvM/0.jpg)](https://www.youtube.com/watch?v=CT5dl_k9gvM)


