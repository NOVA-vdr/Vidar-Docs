```
ftn main():
    println("Hello, World!")
fine
```
Hm... no big difference with other languages

```
ftn main():
    a int8 = 1
    b str = "Hello"
    c int = 1~10
    println(c[5])
    println(b[0])
    println(int(a) + 10)
fine
```
Hmm.. I can't get it

```
ftn main():
    print(sum(1, 2))
fine

ftn sum(A int, B int) (int):
    return A + B
fine
```
Just as I expected

