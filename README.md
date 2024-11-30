# 2024 ML Team Project _ Team 09
## 특징 분석
## Continuous Features

**X1 : sequence of packet sizes**

**X2 : sequence of packet timestamps**

**X3 : sequence of cumulative packet sizes**

**X4 : sequence of bursts**

--------
### Categorical Features

**X5 : Number of Incoming Packets as a Fraction of the Total Number of Packets**

**X6 : Number of Outgoing Packets as a Fraction of the Total Number of Packets**

**X7 : Standard Deviation of the Outgoing Packet Ordering List**

**X8 : Sum of All Items in the Alternative Concentration Feature List**

**X9 : Average of the Outgoing and Total Number of Packets**

----------------------------------

### Continuous feature testing - @minae-mina

**리포지토리 설명** <br> <br>
**ClosedWorld.ipynb** <br>
ClosedWorld 환경의 실험을 위한 데이터 전처리 및 모델(RandomForest)
- Objective
  classify the 95 monitored websites.
- Data Used
  **mon_standard.pkl**: data from "monitored" websites.
   - Class count: 95
   - Instance count: 19,000 (95 websites, each with 10 subpages which are non-index pages, observed 20 times each)
- Features
  - X1_mon : the sequence of **packet timestamps**
  - X2_mon : the sequence of **packet size * direction**
  - X3_mon : the sequence of **cumulative packet sizes**
  - X4_mon : the sequence of **bursts**

- Steps
  1. 준비
      - 데이터 업로드
      - 파일 경로 설정
  2. 데이터 전처리
      - Feature Extraction
      - Sequence Length Normalization
  3. Random Forest 모델 실험
      - X1_mon
      - X1_mon + X2_mon
      - X1_mon + X2_mon + X3_mon
    
**OpenWorld.ipynb** <br>
OpenWorld 환경의 실험(Binary Classification | Multi-Class Classification)을 위한 데이터 전처리 및 모델(SVM or RandomForest)
1. 데이터 전처리는 categorical_feature.ipynb 을 참고함
2. Categorical Features Continuous Features
2. SVM 모델 결과가 좋지 않아 RandomForest 모델을 시도함
---------------

### Categorical feature testing - @mminnjji

**리포지토리 설명**

**최종 파일** <br>
final_categorical.ipynb → 안의 텍스트/ 코드로 open-world svm/random forest / closed-word의 random forest 모델 구현 

**feature 테스트** <br>
feature_test.ipynb → 실제 모델에 적용시켜보며 유효한 지표 선정

**feature 제작 + 시각화하여 추출확인** <br>
categorical_feature.ipynb
---------------


### Model Experimentation and Findings - @jisu-1104 @soviet0205

**파일** <br>
s_final_categorical.ipynb → final_categorical.ipynb 를 수정하여 random forest 모델로 feature 1~9 를 사용한 실험을 함 <br>
finding을 찾아 문서로 작성함
