
# 마스크 착용 분류

사용자의 마스크 착용 유무, 연령대 및 성별 예측 task

## 사용 모델
ResNet50, EfficientNet B4

## 다양한 시도
- Augmentation

Centercrop, IAAPerspective, horizontal flip

- Semi Supervised Learning

F1 socre가 높은 모델의 pred을 살펴보고 0.68 이상인 이미지들은 training data로 재활용

- Age Filter

30세 미만, 30세 이상 60세 미만, 60세 이상으로 연령대를 분류해야했음.

하지만 age의 최대값은 60세 였기에 60세 이상의 data가 부족했음, 이에 age를 58세 기준으로 나눔

- Loss
data 불균형을 해결하기 위해 Focal loss 사용

-Ensemble
hard voting

## 개선해야할 사항
- jupyter notebook 말고 python 파일로 작업하기
- Semi-supervised learning의 overfitting
- 다양한 ensemble 기법 사용


