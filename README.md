# SKT FLY AI 4기 - 품절남녀) 코코 박사 통합 판단 모델 성능 비교

## Data Preprocessing
- 567개의 데이터에서 정제된 483개의 데이터를 산출
- not sleeping 데이터 420개, sleeping 데이터 63개, 데이터 불균형 발생
- 이를 해결하기 위해 3가지 Oversampling 기법을 적용
  -  Random OverSampling
  -  SMOTE OverSampling
  -  ADASYN OverSampling
## ML 모델 비교
- 오버 샘플링된 데이터에 ML 모델을 적용해 성능 비교
  - SVM (SVC)
    - RBF kernel
    - Linear kernel
    - Polynomial kernel
  - XGBoost
  - LightGBM
  - CatBoostClassifier
- No Hyper Params Tuning !
## 비교 결과
<div align="center">
  
  <img width=70% src='https://github.com/dlawork9888/drcoco_model_comparison/assets/127077818/5ec10c6e-ed4f-4841-8a9e-8e1cb06f9417'>
  
  <img width=70% src='tps://github.com/dlawork9888/drcoco_model_comparison/assets/127077818/2149e905-dcda-479e-8c6e-3bc8253269e1'>
  
  <img width=70% src='https://github.com/dlawork9888/drcoco_model_comparison/assets/127077818/50ed420d-6684-4e6d-86d3-e49ca4b1991f'>
  
</div>

