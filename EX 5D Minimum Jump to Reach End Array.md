# EX 5D Minimum Jump to Reach End Array
## DATE:
## AIM:
To write a python program for finding the minimum number of jumps needed to reach end of the array using Dynamic Programming.


## Algorithm
1.Create a jumps[] array.

2.Initialize an array jumps[] where each element is set to a large number (inf), except for the first element, which is set to 0. This represents the minimum number of jumps needed to reach each index.

3.Start iterating through the array.

4.Loop through each element of the array (starting from index 1).

5.For each element arr[i], check if it's possible to reach index i from any earlier index j (i.e., i <= j + arr[j]).

6.If reachable, update jumps[i] to be the minimum of its current value and jumps[j] + 1.

7.The value in jumps[n-1] will give the minimum jumps required to reach the end.

8.If it is still inf, return -1 because it's not possible to reach the end.

## Program:
```
/*
To implement the program to finding the minimum number of jumps needed to reach end of the array.


Developed by: Daniel C
Register Number:  212223240023
def minJumps(arr, n):
    ##########  Add your code here ##############
    
    jumps = [0 for i in range(n)]
 
    if (n == 0) or (arr[0] == 0):
        return float('inf')
 
    jumps[0] = 0
    for i in range(1, n):
        jumps[i] = float('inf')
        for j in range(i):
            if (i <= j + arr[j]) and (jumps[j] != float('inf')):
                jumps[i] = min(jumps[i], jumps[j] + 1)
                break
    return jumps[n-1]
    
    
arr = []
n = int(input()) #len(arr)
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr,n))

*/
```

## Output:

<img width="1130" height="544" alt="image" src="https://github.com/user-attachments/assets/34119b48-8204-400b-b878-691dcc8d8e4a" />


## Result:
Thus the program was executed successfully for finding the minimum number of jumps to reach end.
