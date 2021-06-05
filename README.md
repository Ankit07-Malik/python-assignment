Q. Given an integer n, print a nXn matrix with squares (outermost to innermost) having value n,then n-1 and so on. 
N = int(input("enter N value"))
k = (2*N)-1
low=0
high=k-1
value=N
matrix = [[0 for i in range(k)] for j in range (k)]
for i in range (N):
    for j in range (low , high+1):
        matrix[i][j] =value
    for j in range (low+1 , high+1):
        matrix[i][j] =value
    for j in range (low+1 , high+1):
        matrix[high][j] =value
    for j in range (low+1 , high):
        matrix[j][high] =value
    low=low+1
    high=high-1
    value=value-1
for i in range(k):
    for j in range(k):
        print(matrix[i][j],end=" ")
    print()    
  
 ## k-map
q= can profile A acess profile B
a=is Friend b=is Blocked c=is Admin d=is MarkXuckerberg
    a b c d q
    0 0 0 0 0
    0 0 0 1 1
    0 0 1 0 1
    0 0 1 1 1
    0 1 0 0 0
    0 1 0 1 1
    0 1 1 0 0
    0 1 1 1 1
    1 0 0 0 1
    1 0 0 1 1
    1 0 0 0 1
    1 0 0 1 1
    1 1 1 0 0
    1 1 1 1 1
    1 1 0 0 0
    1 1 0 1 1
    if d or (b not c) or (a and not b):
        print("has access")
    else:
        print("access denied")
