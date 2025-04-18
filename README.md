# [Kaggle] Santander Customer Transaction Prediction
- 데이터로 AI 예측 모델 만들기
- train & Test 데이터 아래에서 다운로드
- https://www.kaggle.com/competitions/santander-customer-transaction-prediction
- reference: https://github.com/saadbinmanjur/Kaggle-Competition-Santander-Customer-Transaction-Prediction/tree/main
---
[문제]

<img width="594" alt="atm_image" src="https://github.com/user-attachments/assets/226d0e74-7bff-4aee-bd38-3b9d77b37a21" />

At Santander our mission is to help people and businesses prosper. We are always looking for ways to help our customers understand their financial health and identify which products and services might help them achieve their monetary goals.

Our data science team is continually challenging our machine learning algorithms, working with the global data science community to make sure we can more accurately identify new ways to solve our most common challenge, binary classification problems such as: is a customer satisfied? Will a customer buy this product? Can a customer pay this loan?

In this challenge, we invite Kagglers to help us identify which customers will make a specific transaction in the future, irrespective of the amount of money transacted. The data provided for this competition has the same structure as the real data we have available to solve this problem.

---

[내 풀이]
- 독립변수: LGBM 의 feature_importance_ 사용해서 영향력 있는 독립변수 100개 뽑음.
- 결측치: 없음
- 이상치: 처리 안함
- 정규화: StandardScaler
- 데이터 불균형: DownSampling_ 타겟이 0인걸 1있는 갯수만큼 랜덤하게 지움
- 모델: GNB (가우시안 나이브 베이즈) 사용_ 상관계수가 전부 낮아서 유리

---
독립변수 100개, 모델 훈련 시
- <img width="837" alt="0 79res" src="https://github.com/user-attachments/assets/3f23369b-9b93-42e3-9d1d-22ac470de5e8" />

독립변수 200개, 모델 훈련 시
- <img width="836" alt="0 80res" src="https://github.com/user-attachments/assets/1a358036-2b14-4d47-b562-ef3327ed2f96" />
