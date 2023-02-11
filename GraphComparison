import numpy as np
import pandas
import math
import matplotlib.pyplot as plt

def is_prime(x):  
    if x < 2:  
        return False  
    for n in range(2, (x)-1):  
        if x % n == 0:  
            return False  
    return True

def arrs(n):
  m = n//2
  top, bottom, v = [None]*m, [None]*m, [None]*m
  for i in range(m):
    top[i] = 1+i+m
    bottom[i] = 1+n-top[i]
    v[i] = (top[i]**2) + (bottom[i]**2)
  return v

print("Enter an integer value to see the primes generated.")
num = int(input()) # Takes user input value to determine values. 
num0 = num-2
func_arr = [None]*num0
log_arr = [None]*num0
for i in range(2, num):
  if (i % 2 == 0):
    tally = 0
    v = [None]*(i//2)
    v = arrs(i)
    print(len(v))
    for j in range(i//2):
      if(is_prime(v[j])):
        tally += 1

    func_arr[i-2] = tally
    log_arr[i-2] = i/np.log(i)
    print("Testing #", i, "Num Primes: ", tally, "Expected: ", log_arr[i-2])

x = np.arange(2, num)
y = np.array(func_arr)

x1 = np.arange(2, num)
y1 = np.array(log_arr)

# plotting
plt.xlabel("Numbers")
plt.ylabel("Number of Primes")
plt.scatter(x, y, color="orange")
plt.scatter(x1, y1, color="grey")
plt.show()
