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

