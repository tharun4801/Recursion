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

