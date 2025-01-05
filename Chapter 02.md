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
> Life is too short
> 
> You need python

#### 1. 줄을 바꾸기 위한 이스케이프 코드 \n 삽입하기
```python
>>> multiline = "Life is too short\nYou need python"
```
* 읽기가 불편하고 줄이 길어지는 단점이 있음

#### 2. 연속된 작은따옴표 3개 또는 큰따옴표 3개 사용하기
* 작은따옴표 3개를 사용한 경우
```python
>>> multiline = '''
... Life is too short
... You need python
... '''
```

* 큰따옴표 3개를 사용한 경우
```python
>>> multiline = """
... Life is too short
... You need python
... """
```

* 이스케이프 코드란? 프로그래밍할 때 사용할 수 있도록 미리 정의해 둔 '문자 조합'
코드 | 설명 
----------------- | ------------------ 
\n | 문자열 안에서 줄을 바꿀 때 사용
\t | 문자열 사이에 탭 간격을 줄 때 사용
\\ | \를 그대로 표현할 때 사용
\' | 작은따옴표(')를 그대로 표현할 때 사용
\" | 큰따옴표(")를 그대로 표현할 때 사용
\r | 캐리지 리턴(줄 바꿈 문자, 커서를 현재 줄의 가장 앞으로 이동)
\f | 폼 피드(줄 바꿈 문자, 커서를 현재 줄의 다음 줄로 이동)
\a | 벨 소리(출력할 때 PC 스피커에서 '삑' 소리가 난다)
\b | 백 스페이스
\000 | 널 문자

___

### 02-2-4. 문자열 연산하기
#### 문자열 더해서 연결하기
```python
>>> head = "Python"
>>> tail = " is fun!"
>>> head + tail
'Python is fun!'
```

#### 문자열 곱하기
```python
>>> a = "python"
>>> a * 2
'pythonpython'
```

#### 문자열 길이 구하기
* 문자열 길이는 len 함수를 사용하여 구할 수 있음
* 문자열의 길이에는 공백 문자도 포함됨
```python
>>> a = "Python is too short"
>>> len(a)
17
```

___

### 02-2-5. 문자열 인덱싱(indexing)과 슬라이싱(slicing)
#### 문자열 인덱싱
```python
>>> a = "Life is too short, You need Python"
```
* L은 첫 번쨰 자리를 뜻하는 숫자 0, 그 뒤로 번호가 붙음

```python
>>> a = "Life is too short, You need Python"
>>> a[3]
'e'
```
> a[0]:'L', a[1]:'i', a[2]:'f', a[3]:'e', a[4]:' ', ....

#### 문자열 인덱싱 활용하기
```python
>>> a = "Life is too short, You need Python"
>>> a[0]
'L'
>>> a[12]
's'
>>> a[-1] /// -는 문자열 뒤에서부터!!
'n'
>>> a[-2]
'o'
>>> a[-5]
'y'
```

#### 문자열 슬라이싱
* 한 문자가 아닌 한 단어를 뽑아 내는 방법
```python
>>> a = "Life is too short, You need Python"
>>> b = a[0] + a[1] + a[2] + a[3]
>>> b
'Life'

================================================
<슬라이싱 기법>
>>> a = "Life is too short, You need Python"
>>> a[0:4] // 0 <= a < 4
'Life' 
```
* 슬라이싱 기법으로 a[시작_번호:끝_번호]를 지정할 때 끝 번호에 해당하는 문자는 포함하지 않음

#### 문자열을 슬라이싱하는 방법
* 슬라이실할 때 항상 시작 번호가 0일 필요는 없음
```python
>>> a[0:2]
'Li'
>>> a[5:7]
'is'
>>> a[12:17]
'short
```

* a[시작_번호:끝_번호]에서 끝 번호 부분을 생략하면 시작 번호부터 그 문자열의 끝까지 뽑아냄
```python
>>> a[19:]
'You need Python'
```

* a[시작 번호:끝 번호]에서 시작 번호를 생략하면 문자열의 처음부터 끝 번호까지 뽑아냄
```python
>>> a[:17]
'Life is too short'
```

* a[시작 번호:끝 번호]에서 시작 번호와 끝 번호를 생략하면 문자열의 처음부터 끝까지 뽑아냄
```python
>>> a[:]
'Life is too short, You need Python'
```

* 슬라이싱에서도 인덱싱과 마찬가지로 -(빼기) 기호를 사용할 수 있음
```python
>>> a[19:-7]
'You need'
```

#### 슬라이싱으로 문자열 나누기
```python
>>> a = "20230331Rainy"
>>> year = a[:4]
>>> date = a[4:8]
>>> weather = a[8:]
>>> year
'2023'
>>> date
'0331'
>>> weather
'Rainy'
```
* 문자열 중 특정 문자를 바꾸고 싶을 때
```python
>>> a = "Pithon"
>>> a[:1]
'P'
>>> a[2:]
'thon'
>>> a[:1] + 'y' + a[2:]
'Python'
```
___

### 02-2-6. 문자열 포매팅(String formatting)이란?
* 문자열 안의 특정한 값을 바꿔야 하는 경우, 이것을 가능하게 해주는 것을 말함
* 즉, 문자열 안에 어떤 값을 삽입하는 방법
___

### 02-2-7. 문자열 포매팅 따라 하기
#### 1.  숫자 바로 대입
```python
>>> "I eat %d apples. % 3
'I eat 3 apples.'
```

#### 2. 문자열 바로 대입
```python
>>> "I eat %s apples." % "five"
'I eat five apples.'
```

#### 3. 숫자 값을 나타내는 변수로 대입
```python
>>> number = 3
>>> "I eat %d apples." % number
'I eat 3 apples.'
```

#### 4. 2개 이상의 값 넣기
```python
>>> number = 10
>>> day = "three"
>>> "I ate %d apples. so I was sick for %s days." % (number, day)
'I ate 10 apples. so I was sick for three days.'
```
___

### 02-2-8. 문자열 포맷 코드
코드 | 설명 
----------------- | ------------------ 
%s | 문자열(string)
%c | 문자 1개(character)
%d | 정수(integer)
%f | 부동소수(floating-point)
%o | 8진수
%x | 16진수
%% | Literal %(문자 % 자체)

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
