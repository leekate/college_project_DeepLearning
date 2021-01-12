# college_project_DeepLearning
# 수업 중 웹캠으로 졸음 인식 및 집중 보조 프로그램

## 기획 이유:
covid-19으로 인해 온라인 강의, 녹화 강의를 이용하는 학생들이 많다. 하지만 온라인 수업에서 수업 태도를 통제하기 어렵다는 의견이 꾸준히 제시되고 있다. 
학생들이 수업 시간에 집중할 수 있도록 시스템을 마련해 적은 시간에 많은 지식을 습득할 수 있도록 도움을 주고싶어 프로젝트를 기획했다.

## Flow:

1) 얼굴 특징점 찾아 얼굴 인식
2) 특징점이 어떤 반응을 보였을 떄 졸음으로 인식하게 할까
3) 졸음이 인식된다면 어떤 기능을 넣을 것인가
3-1) 알람음을 넣어 졸고 있음을 학생에게 알려줌과 동시에 깨움
3-2) 졸기 시작한 시점과 졸음을 벗어난 시점을 기록해 북마크를 만들어 놓친 부분을 기록해 학습에 도움이 되도록 한다

 
## How:

- 68개의 facial landmark detection을 이용해 특징점을 찾아 졸음 인식
- 68개의 facial landmark detection 훈련을 위해 CelebA 데이터 사용
  X data: 얼굴 위주로 정렬된 데이터
  Y data: 68개의 facial landmark의 x,y 좌표 값


## Data Training:
1) Load data
2) Normalization:
minmax normalization 이용
3) Data Split:
**Training set: 96,535
Validation set: 41,373
Test set: 59,104**

4) Make **Resnet network**
모델 구성:
loss: MSE
optimizer: Adam
epoch: 50
batch_size: 64

![다운로드](https://user-images.githubusercontent.com/46522501/104328648-5f8f9000-552f-11eb-955d-54e337ec1b96.png)



## Functions
추가 예정
