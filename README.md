from cmath import sqrt
import random
import math
def isEven(number):
    if(number%2==0):
        return True
    else:
        return  False

def isPositive(number):
    if(number<0):
        return False
    else:
        return True

def isprime(number):
    count=0
    for i in range(2,math.floor(math.sqrt(number))+1):
        if(number%i==0):
            count=1
            break
    if(count==0):
        return True
    if (count<0):
        return False
    else:
        return False



def main():
    a=int(input("Enter Lower Range "))
    b=int(input("Enter Higher Range "))
    r=random.randint(a,b)
    print(f"range is({a},{b}) and randomly picked number is {r}")
    if(isEven(r)):
        print(f'{r} is an Even number')
    else:
        print(f'{r} is a Odd number')
    if(isPositive(r)):
        print(f'{r} is a positive number')
    else:
        print(f'{r} is a negative number')
    if(r<1):
        print(f'{r} is neither prime nor composite')
    elif(isprime(r)):
        print(f'{r} is a prime number')
    else:
        print(f'{r} is a composite number')


main()

