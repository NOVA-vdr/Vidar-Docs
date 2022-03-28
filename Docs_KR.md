`Vidar` v1.0 Docs_KR
# 자료형, 변수


## 변수

`<이름> <타입> = <값>`

위 형식으로 변수를 선언과 동식 대입한다.
```
fn main():
    a int8 = 10
    b str32 = "안녕하세요"
    c float = 3.141592
    d bool = false
    e null = null
fine
```

한 번 선언된 변수는 타입 지정 없이 값을 대입할 수 있다.

```
fn main():
    a int = 3
    a += 4
    a = a - 2
    println(a)
fine
```

> 5

## 자료형
#
+ ### int - int8, int16, in32, int64
+ ### str - str32, str64
+ ### float
+ ### bool
+ ### null

Go언어와 마찬가지로 비트별로 타입 지정이 가능하다.

아래 코드를 참고하여 여러가지 자료형들의 성질을 살펴보자.
```
fn main():
    a int8 = 2
    b int8 = 3
    c str32 = "Hello"
    d str32 = "World"
    e float = 1.001
    println(not a + b == 5)
    println(c + d + "!")
    println(2 ^ 3 + 2 - (3 / b))
    println(typeof(true and false))
    println(true or false)
fine
```
> false

> HelloWorld!

> 9

> bool

> true
## 자료구조
#
## 리스트 
리스트 자료구조는 여러개의 값을 모아논 것이다.

타입 지정은 일반적인 변수와 같다.

일정 구간의 정수들의 수열을 만들고 싶으면 n ~ m..k 를 이용해

n이상, m이하의 정수를 k의 간격으로 지정할 수 있다.

```
fn main():
    a int8 = 1~10..2
    -- a = 1, 3, 5, 7, 9
    println(a[-1])
fine
```

> 9

만약 -1이나 5같은 존재하지 않는 인덱스에 접근하려고 하면, `|<인덱스> % <배열 안의 값의 개수>|`번째 값의 위치에 있는 인덱스에 있는 값을 반환한다.

```
fn main():
    a int8 = 1, 2, 3, 4, 5
    b int8 = 1~5
    c int8 = 0~10..2
    d str32 = "The", "Vidar", "Programming", "Language"
    println(a[2] == b[2])
    println(c)
    println(d[-1])
fine
```
>true

> 0, 2, 4, 6, 8, 10

> Language
---
문자열 자료구조는 리스트와 같은 방법으로 접근할 수 있다.
```
fn main():
    a str32 = "HLEO"
    print(a[0], a[2], a[1], a[1], a[-1])
fine
```
> H E L L O

# 함수

`Vidar`에서에 main()함수는 C언어와 같이 코드가 실행될 때 기본적으로 호출되는 함수이다.

사용자가 직접 함수를 만들고 싶을 때는 다음 형식을 지켜서 만들면 된다.

```
fn main():
    println(sum(11, 1.34))
fine

fn sum(x int8, y float) (float):
    result float = x + y
    return result
fine
```
> 12.34

매개변수 뒤에는 매개변수의 타입을, 함수 이름 뒤에는 반환 타입을 꼭 써줘야 한다.

# 제어문

## 조건문

조건문은 if문으로 통일된다.

다른 언어에 비해 굉장히 다양한 형태로 자유롭게 사용할 수 있다.

```
fn main():
    a int8 = 3
    if a:
    is 1:
        println("a is 1")

    is 2:
        println("a is 2")

    else:
        println("Whatever else")

    fine
fine
```

> Whatever else
#
```
fn main():
    a int8 = 1
    if a == 1:
    is true:
        println("a is 1")
    else:
        println("a isn't 1")
    fine
fine
```

> a is 1
#
이때 아래처럼 `is true:`는 생략이 가능하다.
```
fn main():
    a int8 = 1
    if a == 1:
        println("a is 1")
    else:
        println("a isn't 1")
    fine
fine
```
> a is 1

# 내장함수

다음은 여러가지 내장함수들이다

+ ### print()
+ ### println()
+ ### get()
+ ### typeof()


## print(x)
# 
`x`의 값을 콘솔 화면에 출력한다.

## println(x)
#
`x`의 값을 콘솔 화면에 출력하고, 줄을 바꾼다.

## get()
#
콘솔에 입력한 값을 반환한다.
## typeof(x)
#
`x`의 타입을 `str` 형식으로 반환한다.


# 그 외

## 주석

```
--한줄 주석

---
여
러
줄

주
석
---
```
## 들여쓰기
#
들여쓰기는 `:`와 `fine`기준으로 이루어진다.

그리고 아래 `if`문과 `test()` 함수처럼 모든 들여쓰기는 개인의 취향에 따라 작성이 가능하다.

```
fn main():
    if a:
        is 3:
            println(3)
    
    is 4:
        println(4)
    else:
        println()
    fine

    println(test())
fine

fn test() (bool):
a int = 2
b int = 4
    return a == b
fine
```
