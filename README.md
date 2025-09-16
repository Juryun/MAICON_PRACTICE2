# 🏆 Loan Approval Prediction

## 📌 Overview
금융기관은 대출 승인 여부를 결정할 때 다양한 요인을 고려합니다.  
신청자의 나이, 소득, 학력, 고용 형태, 신용 점수 등의 변수는 대출 심사에 중요한 역할을 합니다.  

이 대회에서는 주어진 고객 정보와 대출 관련 특성을 바탕으로, 대출이 승인될지(`1`) 혹은 거절될지(`0`)를 예측하는 모델을 개발하는 것이 목표입니다.  

참가자들은 머신러닝 분류 알고리즘을 활용하여 **Loan Status**를 예측해야 합니다.

---

## 📂 Data Description
데이터셋은 학습용(`train.csv`)과 평가용(`test.csv`)으로 구성되어 있습니다.  
각 행은 한 명의 대출 신청자에 대한 정보를 포함합니다.

### Features
- **person_age** : 신청자의 나이  
- **person_gender** : 성별  
- **person_education** : 학력 수준  
- **person_income** : 연간 소득  
- **person_emp_exp** : 고용 경력(연수)  
- **person_home_ownership** : 주택 소유 여부  
- **loan_amnt** : 신청한 대출 금액  
- **loan_intent** : 대출 목적 (예: 교육, 의료, 사업 등)  
- **loan_int_rate** : 대출 금리(%)  
- **loan_percent_income** : 소득 대비 대출 상환 비율  
- **cb_person_cred_hist_length** : 신용 기록 보유 기간 (년 단위)  
- **credit_score** : 신용 점수  
- **previous_loan_defaults_on_file** : 과거 대출 연체 이력 (Yes/No)  

### Target
- **loan_status** : 대출 승인 여부 (`1`: 승인, `0`: 거절)  

---

## 🎯 Evaluation
모델의 성능은 **Accuracy**로 평가됩니다.  

\[
Accuracy = \frac{ \text{Number of Correct Predictions} }{ \text{Total Predictions} }
\]

---

## 📑 Submission Format
최종 제출 파일(`submission.csv`)은 학습 데이터와 동일한 컬럼 구조를 가져야 하며, `loan_status`만 참가자의 예측 값으로 채워야 합니다.

예시:

| person_age | person_gender | person_education | person_income | person_emp_exp | person_home_ownership | loan_amnt | loan_intent | loan_int_rate | loan_percent_income | cb_person_cred_hist_length | credit_score | previous_loan_defaults_on_file | loan_status |
|------------|---------------|------------------|---------------|----------------|-----------------------|-----------|-------------|---------------|---------------------|-----------------------------|--------------|--------------------------------|-------------|
| 24         | male          | Master           | 58914         | 2              | OWN                   | 4400      | VENTURE     | 5.99          | 0.07                | 4                           | 656          | Yes                            | 0           |
| 32         | female        | Bachelor         | 72000         | 5              | RENT                  | 10000     | EDUCATION   | 8.25          | 0.14                | 8                           | 710          | No                             | 1           |
| ...        | ...           | ...              | ...           | ...            | ...                   | ...       | ...         | ...           | ...                 | ...                         | ...          | ...                            | ...         |

- 제출 파일에는 테스트 데이터셋의 모든 행이 포함되어야 합니다.  
- **loan_status**는 반드시 `0` 또는 `1`로 예측 값을 채워야 합니다.  

---
