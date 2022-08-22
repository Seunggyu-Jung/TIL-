# 6-20 학습일지
유튜브 학습 코드(파이썬)

## 1. 숫자처리함수 

- abs : 절대값, `print(abs(-5)) = 5`
- pow : 제곱, `print(pow(4,2)) = 16`
- max : 최댓값, `print(max(5,12)) = 12`
- min : 최솟값, `print(min(5, 12)) = 5`
- round : 반올림, `print(round(3.14)) = 3`

## 2. 숫자처리함수 모듈

- 상단에 `from math import *` 이라는 모듈을 작성하는 것이 시작
- floor : 내림, `print(floor(4.99) = 4`
- cell : 올림, `print(ceil(3.14)) = 4`
- sqrt : 제곱근 도출, `print(sqrt(16)) = 4`

## 3. 랜덤함수 모듈

- 상단에 `from random import *` 이라는 모듈을 작성하는 것으로 시작
- random : 0.0 ~ 1.0 미만의 임의의 값 생성, `print(random()*10) = 0.0 ~ 10.0 미만의 임의의 값 생성`
- `int(random()*10)` : 0 ~ 10 미만의 임의의 정수값 생성
- `int(random()*10) + 1` : 1 ~ 10 이하의 임의의 값 생성
- `randrange(1,46)` : 1 ~ 46 미만의 임의의 값 생성
- `randint(1,45)` : 1 ~ 45 이하의 임의의 값 생성, 
- 보통은 randint 함수를 많이 쓴다.