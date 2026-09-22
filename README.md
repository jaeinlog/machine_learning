# Machine Learning Practice

머신러닝의 전체 흐름을 이해하기 위해 진행한 실습을 기록합니다.

## 학습 흐름

데이터 확인 → X·y 설정 → 데이터 분할 → 전처리 → 모델 학습 → 예측 → 평가 → 해석

## 프로젝트 목록

### ML01. Fish Weight Ridge Regression

물고기의 길이·높이·너비를 이용해 무게를 예측한 회귀 실습입니다.

- Target: `Weight`
- Features: `Length1`, `Length2`, `Length3`, `Height`, `Width`
- Models: Mean Baseline, LinearRegression, Ridge
- Metrics: MAE, RMSE, R²
- Notebook: [ml01_fish_weight_ridge.ipynb](./ml01_fish_weight_ridge.ipynb)

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Baseline | 329.77 | 381.47 | -0.0231 |
| Ridge | 104.89 | 132.51 | 0.8766 |
| LinearRegression | 103.91 | 129.48 | 0.8821 |

현재 test split에서는 LinearRegression의 RMSE가 가장 작았습니다.  
다만 한 번의 분할 결과이므로 교차검증을 통한 추가 확인이 필요합니다.
