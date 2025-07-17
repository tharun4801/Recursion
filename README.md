# Recursion
# recursive function
def factorial(n):
    if n==0 or n==1:
        return 1
    return n*factorial(n-1)
num=int(input("enter a number:"))
value=factorial(num)
print(value)
OUTPUT:
enter a number: 5
120

#sum of n natural number
def nsum(n):
    if n==0:
        return 0
    return n+nsum(n-1)
n=int(input("enter n:"))
print("sum of frist", n ,"natural numbers is", nsum(n))
OUTPUT:
enter n: 5
sum of frist 5 natural numbers is 15

def rstring(s):
    if len(s)==0:
        return s
    return rstring(s[1:])+(s[0])
text=input("enter a word:")
print(rstring(text))
OUTPUT:
enter a word: missmiss
ssimssim

#recursions
def fibonaci(n):
    if n<=1:
        return n
    else:
        return fibonaci(n-1)+fibonaci(n-2)
n=int(input("enter the terms:"))
for i in range(n):
    print(fibonaci(i),end=' ')
OUTPUT:
enter the terms: 10
0 1 1 2 3 5 8 13 21 34 

#sum of digits in idirect recursion
def dsum(n):
    if n==0:
        return 0
    return n%10+temp(n//10)
def temp(n):
    return dsum(n)
n=int(input("enter a four digit number:"))
print("sum of digits:",dsum(n))
OUTPUT:
enter a four digit number: 9999
sum of digits: 36

#even and odd using without moduluse
def one(n):
    if n==0:
        return True
    else:
        return two(n-1)
def two(n):
    if n==0:
        return False
    else:
        return one(n-1)
n=int(input("enter the number:"))
if one(n):
    print(n,"is even")
else:
    print(n,"is odd")
OUTPUT:
enter the number: 999
999 is odd
    
def even(n):
    if(n&1)==0:
        return True
    else:
        return odd(n)
def odd(n):
    if(n&1)==0:
        return True
    else:
        return even(n)
n=int(input("enter the number:"))
if even(n):
    print(n,"is even")
else:
    print(n,"is odd")
OUTPUT:
enter the number: 66
66 is even

def A(n):
    if n<=0:
        return
    print("Rajesh",n)
    B(n-1)
def B(n):
    if n<=0:
        return 
    print("pakala",n)
    A(n-1)
n=int(input("enter the number:"))
A(n)
OUTPUT:
enter the number: 6
Rajesh 6
pakala 5
Rajesh 4
pakala 3
Rajesh 2
pakala 1

def player_A(n):
    if n<=0:
        print("player A reached 0!! player A losses🤦‍♂️")
        return
    print(f"\n player A's turn. Current number{n}")
    move=int(input("player A,subtract 1 or 2:"))
    while move not in[1,2]:
        move=int(input("player A,subtract 1 or 2:"))
    player_B(n-move)
def player_B(n):
    if n<=0:
        print("player B reached 0!! player B losses🤦‍♂️")
        return
    print(f"\n player B's turn. Current number{n}")
    move=int(input("player B,subtract 1 or 2:"))
    while move not in[1,2]:
        move=int(input("player B,subtract 1 or 2:"))
    player_A(n-move)
start=int(input("enter starting number:"))
player_A(start)
OUTPUT:
enter starting number: 5

 player A's turn. Current number5
player A,subtract 1 or 2: 3
player A,subtract 1 or 2: 2

 player B's turn. Current number3
player B,subtract 1 or 2: 1

 player A's turn. Current number2
player A,subtract 1 or 2: 2
player B reached 0!! player B losses🤦‍♂️
