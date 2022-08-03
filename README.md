# Kaggle repo 소개
직접 해본 Kaggle(캐글) 프로젝트 노트북을 저장하는 공간  

## #1. [Bike Sharing Demand: 자전거 수요 예측 프로젝트](https://github.com/suy379/Kaggle/tree/main/Bike_sharing_demand)  
`[최종 목표] test 데이터의 대여량(count) 값을 예측하라!` / [캐글 컴퍼티션 바로가기](https://www.kaggle.com/competitions/bike-sharing-demand)  
**문제: 회귀(Regression), 평가지표: RMSLE**  

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
- ver.4~5: 결측치가 많은 `windspeed` 변수 머신러닝을 활용해 채우기
- [성능 개선 포스팅](https://suy379.tistory.com/141)

## #2. [Categorical Feature Encoding: 범주형 데이터 분석 프로젝트](https://github.com/suy379/Kaggle/tree/main/Categorical_feature_encoding)  
`[최종 목표] target 데이터의 0, 1 값을 예측하라!` / [캐글 컴퍼티션 바로가기](https://www.kaggle.com/competitions/cat-in-the-dat)  
**문제: 분류(Classification), 평가지표: AUC score**  

1. EDA
