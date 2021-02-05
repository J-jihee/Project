# Yolo v3을 이용한 눈 관상

## 개발환경
- google colab
  - openCV 4.1.2
  - Python 3.6.9
  - yolo-v3
 
 - VS code 
  - Python 3.5.6
  - Numpy 1.19.4
 

## 기능  
- 사람의 얼굴에서 눈을 인식하여 해당하는 관상을 나타냄

![캡처](https://user-images.githubusercontent.com/78400774/107000900-03d1c300-67cc-11eb-884c-86668a63c80c.PNG)


## Data set
- 총 22개의 사진 (이미지 한 장당 3~4개의 데이터 포함)
- 2개의 test set
- 20개의 train set
- Learning_rate = 0,001
- max_batches = 1200 ( class : 6 * 2000)
