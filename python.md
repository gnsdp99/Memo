# Python

- 문자열로 입력받고 정수 리스트로 저장    
>> map 함수
```python
n = list(map(int, input())
```

- 시퀀스 자료형 정렬 기준
>> key param
```python
sorted(<type>, key = <function>, reverse = <bool>)
```
or
```python
<type>.sort(key = <function>, reverse = <bool>)
```
ex.
```python
arr = [[10, "b"], [20, "c"], [30, "a"]]
arr.sort(key = lambda x:x[1]) # 알파벳을 기준으로 정렬
print(arr)
>> [[30, "a"], [10, "b"], [20, "c"]]
```
- 두 변수의 값 바꾸기
```python
a, b = b, a
```
