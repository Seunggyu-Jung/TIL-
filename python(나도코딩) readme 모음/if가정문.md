# 나도 코딩 파이썬: 6강 if 가정문

# 1. if문

- if문 : input으로 상태 작성, 작성시 한칸은 띄어넣기(터미널에서 값을 입력해야하기 때문)
```
weather = input("오늘의 날씨는 어떤가요? ")
if weather == "비":
   print("우산을 챙기세요!")
elif weather == "미세먼지":
    print("마스크를 챙기세요!")
else :
     print("준비물이 없어요!")
```
- input에 입력할 값이 숫자일 경우, input을 int로 정수화 시켜야한다.
```
temp = int(input("오늘의 기온은 몇도인가요? "))
if temp >= 30:
    print("더우니까 나가지 마세요!")
elif temp <30 and temp >= 20:
    print("날씨가 아주 좋아요!")
elif temp < 20 and temp >= 10:
    print("날씨가 쌀쌀해요!")
else:
    print("추우니까 나가지 마세요!")
```

# 2. for문 
반복문: 행동이 끝날때까지 반복시킨다.
for은 in 을 이용하여 변수의 범위를 지정한다.

```
for waitting_no in [1,2,3,4,5]:
    print("대기번호 : {0}".format(waitting_no))
    -> 대기번호 : 1 , 2 , 3 , 4 , 5
```
- 범위를 쓰기 귀찮으면 range()로 나타내도 상관없다. range()는 ()미만까지의 수 나열
```
for waitting_no in range(1,5):
    print("대기번호 : {0}".format(waitting_no))
    -> 대기번호 : 1 , 2 , 3 , 4
```
# 3. While문
한 행동이 조건을 만족할 때까지 무한히 반복함

```
index라는 변수에 숫자를 주고, 해당 번호가 0일때까지 반복하게 하고,
0일때 커피를 폐기시키는 경우

customer = "토르"
index = 5
while index >= 1:
    print("{0}, 주문하신 커피가 나왔습니다. {1}번 남았습니다.".format(customer,index))
    index -= 1  (숫자에서 1씩 내릴때 -=로 표현)
   if index == 0:
        print("커피가 폐기처분 되었습니다.") 
```
- 무한루프 : True를 사용하여 무한히 반복시킴 , 강제 종료(Ctrl + C)
```
순번을 무한히 늘리는 경우

customer = "아이언맨"
index = 1
while True:
    print("{0}, 주문하신 커피가 나왔습니다. {1}번 남았습니다.".format(customer,index))
    index += 1
```

- input을 이용하여 while문을 만들경우 -> 유튜브 다시 참조
```
카운터에 손님이 왔을때 구별하는 방법, 토르가 나올때까지 반복한다

customer = "토르"
person = "Unknown"
while person != customer:
    person = input("이름이 어떻게 되세요? ")
    print("{0}, 주문하신 커피가 나왔습니다.".format(customer))    
```

# 4. cotinue & break문
- continue는 주어진 사람을 제외하고 끝날때까지 반복한다.
- break는 주어진 작업을 도중에 멈추는 기능을 한다.

```
absent = [2,4,5]
no_book = [7]
for student in range(1,11):
    if student in absent:
        continue
    elif student in no_book:
        print("오늘 수업은 여기까지, {0} 교무실로 따라와".format(student))
        break
    print("{0}, 책을 읽어보렴".format(student))

->
1, 책을 읽어보렴
3, 책을 읽어보렴
6, 책을 읽어보렴
오늘 수업은 여기까지, 7 교무실로 따라와
```

# 5. 한줄 for문 
변수 i를 이용하여, 한줄로 표현

- 출석부 번호에 100을 더하기로 함 ex) 1,2,3 ->101, 102, 103
```
student = [1,2,3,4,5]
student = [i+100 for i in student]
print(student)
-> [101, 102, 103, 104, 105]
```

- 학생이름을 길이로 변환 -> len()
```
student = ["iron man", "gundam", "thor"]
student = [len(i) for i in student]
print(student)
-> [8, 6, 4]
```

- 학생 단어를 대문자로 변환 ->.upper()
```
student = ["iron man", "gundam", "thor"]
student = [i.upper() for i in student]
print(student)
-> ['IRON MAN', 'GUNDAM', 'THOR']
```


