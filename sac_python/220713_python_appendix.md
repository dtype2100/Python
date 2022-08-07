# 220713_python_appendix

상태: Python

# 파일 생성

```python
# 파일 생성
f = open("새파일.txt", 'w')
f.close

# 디렉토리 생성
f = open("C:/doit/새파일.txt", 'w')
f.close()

```

# 출력값 작성

```python
f = open("C:/doit/새파일.txt", 'w')
for i in range(1, 11):
    data = "%d번째 줄입니다.\n" % i
    f.write(data)
f.close()

```

# 파일 읽기

```python
# readline
f = open("C:/doit/새파일.txt", 'r')
line = f.readline()
print(line)
f.close()

# readline으로 모든 줄 출력
f = open("C:/doit/새파일.txt", 'r')
while True:
    line = f.readline()
    if not line: break
    print(line)
f.close()

# readlines
f = open("C:/doit/새파일.txt", 'r')
lines = f.readlines()
for line in lines:
    print(line)
f.close()

# \n 제거
f = open("C:/doit/새파일.txt", 'r')
lines = f.readlines()
for line in lines:
    line = line.strip()  # 줄 끝의 줄 바꿈 문자를 제거한다.
    print(line)
f.close()

# read
f = open("C:/doit/새파일.txt", 'r')
data = f.read()
print(data)
f.close()
```

# 파일에 새로운 내용 추가

```python
# a
f = open("C:/doit/새파일.txt",'a')
for i in range(11, 20):
    data = "%d번째 줄입니다.\n" % i
    f.write(data)
f.close()

# with open
with open("foo.txt", "w") as f:
    f.write("Life is too short, you need python")
```

# Class

- 매서드 또는 함수라 부름
- 반복되는 변수나 메서드(함수)를 미리 정해 놓은 틀(설계도)
- 클래스로 만든 결과를 객체(object)라 한다

```python
>>> class Cookie:
>>>    pass
>>> a = Cookie()
>>> b = Cookie()
```

- a객체는  Cookie의 인스턴스다.
- a는 객체(object)이지만, Cookie와 관계를 설명할 때, 인스턴스라 함.
- 클래스 안에 선언된 함수를 메서드라 함
- self는 객체 자신을 나타냄

```python
class Sesac:
  age = 0
  name = ""

  def __init__(self, value1 , value2):
    self.age = value1
    self.name = value2

  def hello(self):
    self.age, self.name
    print("%d살 %s입니다." % (self.age, self.name))
    
    
lee = Sesac(25, "이새싹")
lee.hello()
```

# 용어 정리

- 클래스: 객체를 만들기 위한 사용자 정의 자료형
- 객체: 클래스를 기반으로 만들어진 구체적인 객체
- 메서드: 객체의 기능을 반영하여 클래스 내부에 선언된 함수
- 상속: 어떤 클래스의 특성을 다른 클래스에 전달하는 기법
- 메서드 오버라이딩: 같은 함수에 여러 기능을 부여하는 구현 기법

- 클래스 안에 구현된 함수는 메서드라 한다.

# 모듈

- 모듈 생성 및 활용 방법
1. py 파일 생성
2. 코드 입력
3. 파일 저장
4. 새로운 파일에서 import로 모듈 불러오기

```python
import mod1
print(mod1.add(3, 4))
print(mod1.add(8, 6))

from mod1 import add
add(3, 44)

from mod1 import *
add(3, 3)

import mod2
mod2.func1()
mod2.func2()
mod2.func2()

from mod2 import func1, func2, func3

func1()
func2()
func3()
```

### prompt에서 모듈 활용

```python
# 파일 경로 변경
cd c:\[파일 경로명]
# ex) cd c:\doit

# 파이썬 입력
python

# 모듈 import
import [모듈명]
# ex) import mod1
```

![Untitled](220713_python_appendix%208f8682b5e3394439ac1605df4483c2ad/Untitled.png)

# 모듈 경로 변경

```python
import sys # import
sys.path # 경로 확인
sys.path.append("C:/Python/module") # 경로 설정
```

# 국취제

금요일x, 월요일까지 출석 증명 필요