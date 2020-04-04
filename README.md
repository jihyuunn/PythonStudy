### dequeue

python에서 dequeue를 import하면 queue로 사용 가능

- append, appendleft, pop, popleft

### 나머지 연산

(A+B)%C = (A%C+B%C)%C  
(A-B)%C = (A%C-B%C)%C

### 유클리드 호제

GCD(a,b) = GCD(b,r) -> r = a%b  
r이 0이될 때 b가 최대공약수가 된다  
a * b = GCD(a,b)*LCM (a * b에서 최소공배수 나누면 최대공약수가 된다)  
a,b,c,d 네개 숫자의 GCD를 구할 때 GCD( GCD( GCD(a,b) *c) \*d)

### 소수

N이 소수인지 아닌지 판별할 때 N=a*b이면 루트N까지 나눠지는지 보면 된다  
while i*i <= N: 으로 루프 돌려주면 된다

### 에라토스테네스의 체

N까지, 2의배수 3의배수, 4의배수 ... 계속 지워주면 소수만 남는다

- 마지막에 소수인 숫자 출력할 때 1이 출력되지 않게 조심해야한다

### 문자열

```python
import string
lowercase = string.ascii_lowercase # 소문자 abcdefghijklmnopqrstuvwxyz
uppercase = string.ascii_uppercase # 대문자 ABCDEFGHIJKLMNOPQRSTUVWXYZ
string.ascii_letters #대소문자 모두 abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ
string.digits # 숫자 0123456789
ord(some_character) # 알파벳을 아스키코드로
chr(some_digit) # 숫자를 알파벳으로
```

### Dynamic Programming / Divide&Conquer

DP는 중복가능 e.g. 40명을 10명/30명으로 나누기  
D&C는 중복 불가능 e.g. 왼쪽 / 오른쪽 다른 구성  
DP의 조건 : 겹치는 부분문제(피보나치 F3을 구할 때나 F5를 구할 때 둘다 F1,F2를 구해야한다) / 최적 부분구조(큰 문제의 정답을 작은 문제에서 찾을 수 있어야 하는 것)  
=> 메모이제이션이 필요하다

##### 마지막에 올 수 있는 경우의 수를 알아야 이전의 정답에 더하거나 해주면 된다

### python copy

- shallow copy

```python
a = [1,2,3]
b = a
a[2] = 100
print(b)
# [1,2,100] a를 바꾸면 바꾼 것이 b에도 적용된다
```

- deep copy

```python
a = [1,2,3]
b = [x for x in a]
# a를 변경시켜도 b에 적용이 되지 않는다
```

### 역추적

list에 몇번 index에 있는 숫자로 인해 바뀌었는지 등을 기록하는 것  
변화 순서, 방문 순서 등을 출력해야되거나 할 때 필요하다  
(2263 트리의 순회에서 해당 숫자의 배열을 기록할 수 도 있다)

```python
a = [100, 2, 4]
index[100] = 0
index[2] = 1
index[4] = 2
# for문이나 while문으로 찾아야하는 index찾기를 O(1)만에 찾을 수 있다
```
