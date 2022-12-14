# deep_learning_self_study
책 '혼자 공부하는 머신러닝 + 딥러닝' - 박해선 을 읽고 정리하는 레포입니다.

# 1. 나의 첫 머신러닝
## 1-1 인공지능과 머신러닝, 딥러닝
### - 인공지능이란
1. what?
    - 사람처럼 학습하고 추론할 수 있는 지능을 가진 컴퓨터 시스템을 만드는 기술
    - 태동기, 황금기, 겨울을 거쳐 현재의 AI 붐 탄생
    - 컴퓨터 성능의 한계로 좌절되는 경우가 많음
### - 머신러닝이란
1. what?
    - 규칙을 일일이 프로그래밍하지 않아도 자동으로 데이터에서 규칙을 학습하는 알고리즘 연구
    - 통계학과 깊은 관련
3. how?
    - '사이킷런' : 대표적인 파이썬 머신러닝 라이브러리을 사용해서 쉽게 구현 가능
### - 딥러닝이란
1. what?
    - 많은 머신러닝 중 인공신경망을 기반으로 한 방법들을 통칭
    - 보통은 Layer 2개 이상일 때, 딥러닝이라는 표현을 쓰는 것 같음!
    - 유명한 이미지 모델은 LeNet-5, ImageNet, AlexNet 등
3. how?
    - TensorFlow (Google) - 딥러닝 라이브러리(파이썬)
    - Pytorch (FaceBook) - 딥러닝 라이브러리(파이썬)
### - 요약

## 1-2 코랩과 주피터 노트북
### 코랩
1. what?
    - 클라우드 기반의 주피터 노트북 개발환경
    - 컴퓨터 성능 상관없이, 구글 클라우드로 연결되어서 작업 가능!
### 노트북
    - 메모리 : 12기가, 디스크 공간 100기가
    - 구글 클라우드 가상 서버는 최대 5개
## 1-3 마켓과 머신러닝
    - 생선 분류 문제
        - 한 생선을 보고 그 생선이 어떤 생선이 판단하려면 어떻게 해야할까?
            1. if 문을 여러개 쓰면서, 사람이 직접 규칙을 찾아 코드 작성
                - 예외 사항들이 너무 많고, 이런 예외를 모두 처리해주기 매우 까다로움.
            2. 생선의 길이, 무게 등의 feature를 파악하여 계산
                - import matplotlib.pyplot as plt # matplotlib의 pyplot 함수를 plt로 줄여서 보통 사용
                - scatter(), xlabel(), ylabel(), show() 등의 함수가 있음
                - 길이, 무게의 feature 두개를 파악해서 linear 한 관계를 유추할 수 있음.
                - zip() 함수를 사용하면, lengths = [], weights = [] 를 [length, weight] 의 배열 형태로 만들 수 있음
    - KNN(K-Nearest Neighbors)
        1. what?
            - 거리상 가장 가까운 점들을 계산하여, 새로운 데이터가 어떤 종류의 데이터인지 파악할 수 있는 알고리즘
            - 단점은 k-최근접 이웃 알고리즘은 가장 가까운 직선거리에 대해서 어떤 데이터가 있는지만 살피면 됨! 
            - 이러한 특징 때문에,  데이터가 아주 많은 경우 사용하기가 힘듬
                - 데이터가 크기 때문에, 메모리가 많이 필요하고, 계산 시간이 매우 많이 소요됨 (모든 노드에 대해서 분석하기 때문에)
