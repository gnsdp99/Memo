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
arr.sort(key = lambda x:x[1]) # 1번 인덱스 기준 정렬
print(arr)
>> [[30, "a"], [10, "b"], [20, "c"]]
```
ex2.
```python
arr = [[10, "c"], [20, "b"], [10, "a"]]
arr.sort(key = lambda x:(x[0], x[1])) # 0번 인덱스 기준 정렬 후 1번 인덱스 기준 정렬
print(arr)
>> [[10, "a"], [10, "c"], [20, "b"]]
```
- 두 변수의 값 바꾸기
```python
a, b = b, a
```
- 리스트 중복 값 제거
>> set
```python
arr = ['apple', 'orange', 'apple']
arr = list(set(arr)) # set의 인자로 리스트를 주면 리스트의 원소 단위 그대로 만들어진다.
# set의 인자로 문자열을 줄때만 알파벳 단위로 만들어진다.
print(arr)
>> ['apple', 'orange']
```
- 리스트 인덱스를 빠른 시간안에 가져오기
>> dict 
```python
pos = [2, 3, 0, 3, 1]
temp = sorted(list(set(pos))) # [0, 1, 2, 3]
new = {temp[i]: i for i in range(len(temp))} # list.index() 함수는 O(N)만큼 걸리기 때문에 N이 크면 오래 걸린다.
print(new)
>> {0: 0, 1: 1, 2: 2, 3: 3}
```
