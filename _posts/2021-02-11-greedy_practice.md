---
title : "모험가 길드(그리디 알고리즘)"
layout: collection
permalink: /algorithmtil/3
collection: algorithmtil
entries_layout: grid
classes: wide
category : 
    - 알고리즘
tag : 
    - 알고리즘
toc : true
---



# 모험가 길드(그리디 알고리즘)

> 참고서적: 이것이 취업을 위한 코딩 테스트이다 with Python. 나동빈 지음

- 난이도: 하
- 풀이 시간: 30분
- 시간 제한: 1초
- 메모리 제한: 128MB

### 문제 - 311쪽

### 입력조건

- 첫째 줄에 모험가의 수 N이 주어진다.
- 둘째 줄에 각 모험가의 공포도의 값을 N이하의 자연수로 주어지며, 각 자연수는 공백으로 구분한다

### 출력 조건

- 여행을 떠날 수 있는 그룹 수의 최댓값을 출력

### 풀이 과정(스스로 생각 20%, 정답 참고 80%)

1. 최대한 많은 그룹을 생성해야 하기 때문에 오름차순으로 둘째 줄에 입력되는 공포도의 값들을 정렬한다.
2. 그룹 수와 그룹 안에 포함되는 사람 수에 대한 변수를 생성한다.
3. 모험가의 수가 공포도 이상일 때 그룹이 생성된다.

```python
n = int(input())  # 모험가의 수
fear = list(map(int, input().split()))  # 모험가 수에 맞게 공포도를 입력한다.

group = 0  # 그룹수를 입력한다.
member = 0  # 현재 그룹에 포함된 모험가의 수를 기록한다.

for i in fear:
    member += 1  # 현재 그룹에 모험가를 추가한다.
    if member >= i:  # 만약 현재 그룹에 포함된 모험가의 수가 공포도 이상이라면 그룹이 생성된다.
        group += 1  # 조건이 부합할 경우 그룹의 수를 증가
        member = 0  # 그룹 멤버 수 초기화

print(group)
```