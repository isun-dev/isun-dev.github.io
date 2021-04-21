# 재귀함수

- 반복문의 효과를 내는 것이 재귀 함수 이다.
- 재귀함수 구현 및 동작 설명

```python
1 def DFS(x):
2     if x > 0:
3         DFS(x-1)
4 				print(x, end=' ')
5
6
7 if __name__=="__main__":
8     n = int(input())
9     DFS(n)
```

1. n은 3이라고 가정, 9라인에서 DFS함수를 호출한다.
2. x > 0일경우 DFS함수는 x의 값을 1씩 감소하면서 재귀가 호출이 되는데, 자세한 내용은 아래와 같다.

    <img width="438" alt="_2021-04-21__11 06 25" src="https://user-images.githubusercontent.com/43905552/115569322-12724580-a2f8-11eb-944d-33c99646c382.png">

3. x > 0에 만족하지 않을 경우, 함수가 종료되게 되고, 함수가 종료되면서 STACK에 있는 스택 프레임들이 FILO규칙에 따라 동작을 한다.