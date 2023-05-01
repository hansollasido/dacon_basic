# dacon_basic

데이콘 Basic에 참가했던 대회들 모음입니다.

- [펭귄 몸무게 예측 경진대회](https://dacon.io/competitions/official/235862/overview/description)
- [여행 상품 신청 여부 예측 경진대회](https://dacon.io/competitions/official/235959/overview/description)
- 쇼핑몰 지점별 매출액 예측 경진대회

---

Dacon Basic 대회를 통해 인공지능을 실습하고 공부해보는 기회를 가졌습니다.

- 데이터 분석

![image](https://user-images.githubusercontent.com/101409953/235389963-c3b4b3fb-b2ce-4184-b56d-1b04e158889f.png)

![image](https://user-images.githubusercontent.com/101409953/235390172-43f8ec2a-efd2-4b9b-866f-a41dfa98a352.png)


- 데이터 처리

```python
# 정규화를 위해 sklearn의 StandardScaler를 사용합니다.
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()

scaler.fit(train[['add_promotion']])

scaled = scaler.transform(train[['add_promotion']])

train['Scaled_promotion'] = scaled
```

- 신경망 구조 또는  설계

```python
import time
from sklearn.ensemble import RandomForestClassifier
from sklearn.model_selection import GridSearchCV
start = time.time() # 시작 시간 저장

# 랜덤 포레스트의 parameter 범위를 정의한다.
RF_params = {
    'n_estimators' : [50,100,150,200,300,500,1000],
    'max_features' : ['auto','sqrt'],
    'max_depth' : [8,10,12,14,16],
    'min_samples_leaf' : [1,2,4,8],
    'min_samples_split' : [2,3,5,10]}

# GridSearchCV를 이용하여 dict에Randomforest 모델을 저장한다. 
RF_models = {
    'RF': GridSearchCV(
    RandomForestClassifier(random_state=42), param_grid=RF_params, n_jobs=-1
    ).fit(train_input, train_target).best_estimator_}

print(f'걸린시간 : {np.round(time.time()-start, 3)}초') # 현재시간 - 시작시간(단위 초)
```

- 학습
- 예측
- 결과 제출
