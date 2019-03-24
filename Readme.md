
파이썬 문법 모음
=============

사칙연산
------
 1 . 더하기(+) 2는 3이라는 값을 출력해 보자.   
보통 계산기 사용하듯 더하기 기호만 넣어 주면 된다.  
```python
>>> 1 + 2
3
```
2 . 나눗셈(/)과 곱셈(*) 역시 예상한 대로 결과값을 보여준다.  
```py
>>> 3 / 2.4
1.25
>>> 3 * 9
27
```
우리가 일반적으로 알고 있는 ÷ 기호나 × 기호가 아닌 것에 주의하자.
```py
# 기본적인 사칙연산 sample
print(5 + 6) # 11
print(5 - 2) # 3
print(3 * 8) # 24
print(3 ** 3) # 27 제곱
print(8 / 2) # 4.0 float형
print(8 // 2) # 4 int형
print(8 % 3) # 2 나머지
```
문자형
----
### <b>문자열</b> 이란?  
문자열(String)이란 문자, 단어 등으로 구성된 문자들의 집합을 의미한다. 예를 들어 다음과 같은 것들이 문자열이다.

```py
"Life is too short, You need Python"
"a"
"123"
```
위의 문자열 예문을 보면 모두 큰따옴표(" ")로 둘러싸여 있다. 
근데 그것 말고도 string 형태로 가능

1. 큰따옴표로 양쪽 둘러싸기
```py
"Hello World"
```
2. 작은따옴표로 양쪽 둘러싸기
```py
'Python is fun'
```
3. 큰따옴표 3개를 연속으로 써서 양쪽 둘러싸기
```py
"""Life is too short, You need python"""
```
4. 작은따옴표 3개를 연속으로 써서 양쪽 둘러싸기
```py
'''Life is too short, You need python'''
```
큰따옴표(")로 둘러싸인 문자열은 + 연산과 동일하다
```py
>>> print("life" "is" "too short") # ①
lifeistoo short
>>> print("life"+"is"+"too short") # ②
lifeistoo short
```
위의 예에서 ①과 ②는 완전히 동일한 결과값을 출력한다. 즉, 따옴표로 둘러싸인 문자열을연속해서 쓰면 + 연산을 한 것과 같다.

문자열 띄어쓰기는 콤마로 한다  
```py
>>> print("life", "is", "too short")
life is too short
```
콤마(,)를 이용하면 문자열 간에 띄어쓰기를 할 수 있다.

### <b>Slicing String(문자열 슬라이싱)</b>
```py
a_str = ‘Leopold’
print(a_str[0])
# L
print(a_str[1])
# e
print(a_str[-1])
# d
print(a_str[-2])
# l
```
list는 수정이 가능함 .1
```py
# del 함수 사용 
test = [‘a’, ‘b’, ‘c’, ‘d’, ‘e‘] 
del test[2]
print(test)
# [‘a’, ‘b’, ‘d’, ‘e’]
```

list는 수정이 가능함 .2
```py
test = [1, 2] test.append(3)
# 맨 뒤에 값 추가
print(test)
#[1, 2, 3]
```
list 정렬
```py
test = [3, 1 , 2 , 5 , 4] 
test.sort( )
print(test) 
# [1, 2, 3, 4, 5]
```
tuple 슬라이싱
```py
>> t1 = (1, 2, 'a', 'b')
>>> t1[1:]
(2, 'a', 'b')
```
tuple 더하기
```py
>>> t1 = (1, 2, 'a', 'b')
>>> t2 = (3, 4)
>>> t1 + t2
(1, 2, 'a', 'b', 3, 4)
```
사전형객체 딕셔너리
```py
>>> dic = {'name’:’cy’, ‘phone’:’01020153330', 'birth': ‘0901’}
>>> dic[‘name’] #’cy’

```
if,elif,else 연산자사용  
(예제)  
"돈이 3000원 이상 있거나 카드가 있다면 택시를 타고 그렇지 않으면 걸어 가라"
```py
>>> money = 2000
>>> card = True
>>> if money >= 3000 or card:
...     print("택시를 타고 가라")
... else:
...     print("걸어가라")
...
택시를 타고 가라
>>>
```

또다른 예시
```py
a={'name':str(input('이름')),'gender':str(input('남 혹은 여로 입력'))}

if a['name'] == 'cy' and  a['gender'] == '여':
    print('너구나?')
elif a['name']=='cy' and a['gender']=='남':
    print('또다른 cy')
else :
    print('넌누구?')
```

for in 예시
```py
test_list = [ 1, 2, 3, 4, 5 ]
result = [ num * 3 for in test_list ]
print(result)
# [ 3, 6, 9, 12, 15 ]
```

문제1
```py
a = int(input())
# Print a value:
# print(a)
if a > 1 :
  print(1)
elif a==0 :
  print(0)
else :
  print(-1)
```
문제2 답
```py
a_list=[int(input('연도')),int(input('월')),int(input('일'))]
if (a_list[0]-a_list[1]+a_list[2])%10==0:
  print('대박')
else:
  print('그럭저럭')
```