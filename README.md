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
<div align='center'>
  <span>
    <img width=30% src='https://github.com/dlawork9888/drcoco_model_comparison/assets/127077818/5ec10c6e-ed4f-4841-8a9e-8e1cb06f9417'>
    <img width=30% src='https://github.com/dlawork9888/drcoco_model_comparison/assets/127077818/2149e905-dcda-479e-8c6e-3bc8253269e1'>
    <img width=30% src='https://github.com/dlawork9888/drcoco_model_comparison/assets/127077818/50ed420d-6684-4e6d-86d3-e49ca4b1991f'>
  </span>
</div>

- Random Oversampling
  - LightGBM이 가장 좋은 성능을 보임(acc 0.905)
  - XGBoost와 CatBoostClassifier도 준수한 퍼포먼스를 보여줌(0.893)
- SMOTE Oversampling 
  - CatBoostClassifier가 가장 좋은 성능을 보임(0.887)
  - XGBoost, LightGBM도 준수함(0.881, 0.875)
- ADASYN Oversampling
  - XGBoost, CatBoostClassifier가 acc 0.911로 세 데이터셋 중 가장 좋은 정확도를 보여줌
  - LigthGBM도 0.899로 90%에 가까운 정확도를 산출
- SVM
  - 세 데이터셋에 대해 다른 세 모델(XGBoost, LightGBM, CatBoost)보다 성능이 좋지 않음



