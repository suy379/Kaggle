# Kaggle repo 소개 👋
직접 해본 Kaggle(캐글) 프로젝트 노트북을 저장하는 공간입니다. 분석에 대한 설명은 블로그에 작성하고 있으니, 목차에 걸어둔 링크를 클릭하시면 됩니다 :)  
캐글 컴퍼티션에 도전하고 싶은 분들께 좋은 참고 자료가 되길 바랍니다!  

## #1. [Bike Sharing Demand: 자전거 수요 예측 프로젝트](https://github.com/suy379/Kaggle/tree/main/Bike_sharing_demand)  
**문제: 회귀(Regression), 평가지표: RMSLE**  
`[최종 목표] test 데이터의 대여량(count) 값을 예측하라!` / [캐글 컴퍼티션 바로가기](https://www.kaggle.com/competitions/bike-sharing-demand)  

1. EDA 
  - train data를 바탕으로 사용자들의 사용 패턴을 알아보았다.
  - 수치형 변수(numerical data), 범주형 변수(categorical data)에 따라 시각화하였으며, target인 count와의 관계를 파악하였다.
  - [train data EDA 포스팅](https://suy379.tistory.com/133)

2. Machine Learning - Baseline model
- 아웃라이어 제거, 수치형 변수 scaling, target 변수 로그변환 등의 데이터 전처리
- EDA 결과를 반영해, target이 casual일 때와 registered일 때를 나누어 예측
- 기본 모델: 선형 회귀(Linear Regression)
- [베이스라인 모델링 포스팅](https://suy379.tistory.com/139)

3. Machine Learning - 성능 개선
- ver.2: target을 count로 통일, 여러 모델 중 가장 성능이 좋은 `XGBRegressor` 선택
- ver.3: 겹치는 변수인 month, season 중 `season` 선택
- ver.4~5: `windspeed` 변수의 결측치를 머신러닝을 활용해 채우기
- [성능 개선 포스팅](https://suy379.tistory.com/141)


## #2. [Categorical Feature Encoding: 범주형 데이터 분석 프로젝트](https://github.com/suy379/Kaggle/tree/main/Categorical_feature_encoding)  
**문제: 분류(Classification), 평가지표: AUC score**  
`[최종 목표] target 데이터의 0, 1 값을 예측하라!` / [캐글 컴퍼티션 바로가기](https://www.kaggle.com/competitions/cat-in-the-dat)  


1. EDA
- 주어진 모든 변수는 범주형 데이터이다. 범주형 데이터의 각 카테고리 비율을 가장 잘 보여줄 수 있는 bar plot 형태로 시각화
- 범주형 변수와 target과의 관계 파악: 1의 값을 갖고 있는 비율 시각화
- [EDA 포스팅](https://suy379.tistory.com/153)

2. Machine Learning - Baseline model
- 머신러닝을 위해, 각 범주형 변수에 알맞은 형태로 인코딩(Encoding)
- 기본 모델: 로지스틱 회귀(Logistic Regression)

3. Machine Learning - 성능 개선
- ver.1: 명목형 변수(nom_*)의 개수 조정
- ver.2~3: 로지스틱 회귀의 하이퍼 파라미터 튜닝
