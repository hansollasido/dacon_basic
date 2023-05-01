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
- 학습
- 예측
- 결과 제출
