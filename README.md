# Classification-of-mask-wearing
pstage1

사용한 모델 아키텍처 및 하이퍼 파라미터
아키텍처 : resnet50, efficientnet B4

A.	LB 점수 : 각각 0.7710, 0.7574
B.	Augmentation : centercrop과 IAAPerspective, horizontal flip만 사용 (기존에는 clahe togray randombrightnesscontrast. 도 사용하였지만 오히려 성능이 하락됨)
C.	Img_size = 224 * 224
D.	추가 시도
i.	가장 f1 score가 높은 모델의 pred를 살펴보고 0.68이상인 이미지들은 트레이닝 데이터로 재활용 -> private LB의 주요 하락 원인으로 예상 중
ii.	Epoch을 줄일 때 가장 큰 성능 향상을 보았음…
iii.	58세도 60세 이상 클래스로 넣어줌.
iv.	Focal loss를 사용
