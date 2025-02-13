# Colab_analysis
# Prophet과 LSTM 분석을 통한 가격 예측 모델
핵심광물의 최적 구매 시기를 예측하기 위한 가격 예측형 모델 개발

[제 12회 산업통상자원부 공공데이터 활용 아이디어 공모전_데이터 분석_주제2]

# 1. 데이터 수집
- 과거 가격 데이터: 핵심광물의 과거 가격 데이터 (일별, 주별, 월별)
- 수급 데이터: 공급량과 수요량 데이터
- 경제 지표: 금리, 환율, GDP 성장률

# 2. 데이터 전처리
- **결측값 처리**: 결측값을 보완하거나 제거.
- **데이터 정규화**: 값의 범위를 조정하여 모델의 성능을 향상.
- **시계열 분해**: 시계열 데이터를 계절성, 잔차로 분해
  
# 3. 탐색적 데이터 분석 (EDA)
- **시각화**: 시계열 데이터의 트렌드, 계절성, 변동성을 시각화
- **상관관계 분석**: 다양한 변수들 간의 상관관계를 분석

# 4. 시계열 분석
- **Prophet 모델**: 트렌드와 계절성을 감지

# 5. 머신러닝 기법
랜덤 포레스트: 다수의 결정 트리를 결합하여 예측 성능을 향상
XGBoost: 부스팅 알고리즘을 사용하여 예측 정확도를 높임
- **LSTM**: Long Short-Term Memory 네트워크를 사용하여 시계열 데이터를 예측

# 6. 피처 엔지니어링
- **시계열 특성 생성**: 이동 평균, 이동 표준편차, 차분 값 등 시계열 특성을 생성

# 7. 모델 구축 및 평가
- **훈련 및 테스트 데이터 분할**: 데이터를 훈련과 테스트 셋으로 나눔
- **모델 훈련**: 다양한 모델을 훈련시키고 성능을 비교
- **모델 평가**: RMSE, MAE, MAPE 평가지표를 사용하여 모델 성능을 평가

# 8. 최적화 및 배포
- **하이퍼파라미터 튜닝**: Random Search를 사용하여 모델의 하이퍼파라미터 최적화

# 9. 실시간 데이터 처리
- **데이터 스트리밍**: 실시간으로 데이터를 수집하고 처리할 수 있는 파이프라인 구축 (Apache Kafka, Spark Streaming)
- **예측 모델 업데이트**: 새로운 데이터가 들어올 때마다 모델을 업데이트
