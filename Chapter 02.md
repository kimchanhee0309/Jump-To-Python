# 02장 파이썬 프로그래밍의 기초, 자료형

<details>
<summary>02-1 숫자형</summary>
<div markdown="1">    

### 02-1-1. 숫자형은 어떻게 만들고 사용할까?
#### 정수형(integer)
* 정수를 뜻하는 자료형(양의 정수와 음의 정수)
```python
>>> a = 123 // 양의 정수 대입
>>> a = -178 // 음의 정수 대입
>>> a = 0 // 숫자 0 대입
```

#### 실수형(floating-point)
* 소수점이 포함된 숫자를 말함
```python
>>> a = 1.2
>>> a = -3.45

================
// '컴퓨터식 지수 표현 방식'
>>> a = 4.24E10 // 4.24 x 10의 10승
>>> a = 4.24e-10 // 4.24 x 10의 -10승
```

#### 8진수(octal)와 16진수(hexadecimal)
* 8진수를 만들기 위해서는 숫자가 0o 또는 0O으로 시작하면 됨
```python
>>> a = 0o177
>>> print(a)
127 
```

* 16진수를 만들기 위해서는 0x로 시작하면 됨
```python
>>> a = 0x8ff
>>> b = 0xABC
>>> print(b)
2748
```
___ 

### 02-1-2. 숫자형을 활용하기 위한 연산자
#### 사칙 연산
```python
>>> a = 3
>>> b = 4
>>> a + b
7
>>>a - b
-1
>>> a * b
12
>>> a / b
0.75
```

#### x의 y제곱을 나타내는 ** 연산자
* x ** y처럼 사용했을 때 x의 y제곱 값을 리턴함
```python
>>> a = 3
>>> b = 4
>>> a ** b
81
```

#### 나눗셈 후 나머지를 리턴하는 % 연산자
* 나눗셈의 나머지 값을 리턴하는 연산자
```python
>>> 7 % 3
1
>>> 3 % 7
3
```

#### 나눗셈 후 몫을 리턴하는 // 연산자
```python
>>> 7 / 4
1.75

>>> 7 // 4
1
```

</div>
</details>

___

<details>
<summary>02-2 문자열 자료형</summary>
<div markdown="1">    

### 02-2-1. 문자열은 어떻게 만들고 사용할까?
#### 1. 큰따옴표로 양쪽 둘러싸기
> "Hello, World"

#### 2. 작은따옴표로 양쪽 둘러싸기
> 'Python is fun'

#### 3. 큰따옴표 3개를 연속으로 써서 양쪽 둘러싸기
> """Life is too short, You need python"""

#### 4. 작은따옴표 3개를 연속으로 써서 양쪽 둘러싸기
> '''Life is too short, You need python'''
___

### 02-2-2. 문자열 안에 작은따옴표나 큰따옴표를 포함시키고 싶을 때
#### 1. 문자열에 작은따옴표 포함하기
> Python's favorite food is perl
* 위와 같은 문자열을 food 변수에 저장하고 싶을 때
  * 문자열 중 작은따옴표(')가 포함되어 있음
  * 이런 경우에는 문자열을 큰따옴표로 둘러싸야 함
  * 큰따옴표 안에 들어 있는 작은따옴표는 문자열을 나타내기 위한 기호로 인식되지 않음
```python
>>> food = "Python's favorite food is perl"
>>> food
"Python's favorite food is perl"
```
* 큰따옴표가 아닌 작은따옴표로 둘러싸는 경우 'Python'이 문자열로 인식되어 구문 오류가 발생함
```python
>>> food = 'Python's favorite food is perl'
  File "<stdin>", line 1
    food = 'Python's favorite food is perl'
                   ^
SyntaxError: invalid syntax
```

#### 2. 문자열에 큰따옴표 포함하기
> "Python is very easy." he says.
* 위와 같이 큰따옴표가 포함된 문자열의 경우, 작은따옴표로 둘러싸면 됨
```python
>>> say = '"Python is very easy." he says.'
```

#### 3. 역슬래스를 사용해서 작은따옴표와 큰따옴표를 문자열에 포함하기
```python
>>> food = 'Python\'s favorite food is perl'
>>> say = "\"Python is very easy.\" he says."
```
* 역슬래시를 작은따옴표나 큰따옴표 앞에 삽입하면 역슬래시 뒤의 작은따옴표나 큰따옴표는 문자열을 둘러싸는 기호의 의미가 아닌 '나 " 자체를 뜻하게 됨
___

### 02-2-3. 여러 줄인 문자열을 변수에 대입하고 싶을 때

___

### 02-2-4. 문자열 연산하기

___

### 02-2-5. 문자열 인덱싱과 슬라이딩

___

### 02-2-6. 문자열 포매팅이란?

___

### 02-2-7. 문자열 포매팅 따라 하기

___

### 02-2-8. 문자열 포맷 코드

___

### 02-2-9. 포맷 코드와 숫자 함께 사용하기

___

### 02-2-10. format 함수를 사용한 포매팅

___

### 02-2-11. f 문자열 포매팅

___

### 02-2-12. 문자열 관련 함수들

</div>
</details>

___

<details>
<summary>02-3 리스트 자료형</summary>
<div markdown="1">    

### 리스트는 어떻게 만들고 사용할까?
### 리스트의 인덱싱과 슬라이싱
### 리스트 연산하기
### 리스트의 수정과 삭제
### 리스트 관련 함수

</div>
</details>

___

<details>
<summary>02-4 튜플 자료형</summary>
<div markdown="1">    

### 튜플을 어떻게 만들까?
### 튜플의 요솟값을 지우거나 변경하려고 하면 어떻게 될까?
### 튜플 다루기

</div>
</details>

___

<details>
<summary>02-5 딕셔너리 자료형</summary>
<div markdown="1">    

### 딕셔너리란?
### 딕셔너리는 어떻게 만들까?
### 딕셔너리 쌍 추가, 삭제하기
### 딕셔너리를 사용하는 방법
### 딕셔너리 관련 함수

</div>
</details>

___

<details>
<summary>02-6 집합 자료형</summary>
<div markdown="1">    

### 집합 자료형은 어떻게 만들까?
### 집합 자료형의 특징
### 교집합, 합집합, 차집합 구하기
### 집합 자료형 관련 함수

</div>
</details>

___

<details>
<summary>02-7 불 자료형</summary>
<div markdown="1">    

### 불 자료형은 어떻게 사용할까?
### 자료형의 참과 거짓
### 불 연산

</div>
</details>

___

<details>
<summary>02-8 자료형의 값을 저장하는 공간, 변수</summary>
<div markdown="1">    

### 변수는 어떻게 만들까?
### 변수란?
### 리스트를 복사하고자 할 때
### 변수를 만드는 여러 가지 방법

</div>
</details>
