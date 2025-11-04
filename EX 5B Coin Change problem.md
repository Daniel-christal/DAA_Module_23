# EX 5B Coin Change Problem
## DATE:
## AIM:
To compute the fewest number of coins that we need to make up the amount given.


## Algorithm
1.Create an array (dp) to store the minimum number of coins needed for each amount.

2.Set dp[0] = 0 because no coins are needed to make 0.

3.Set all other values in dp to infinity (inf) because we don’t know the minimum coins yet.

4.For each coin in the given list of coins:Start from the coin value and go up to the target amount.

5.For each amount, update the dp array:If using the coin results in fewer coins than what is already stored, update it.

6.If dp[amount] is still infinity, return -1 (this means it’s not possible to make that amount with the given coins).

7.Otherwise, return the value in dp[amount], which is the minimum number of coins needed.

## Program:
```
/*
Create a python function to compute the fewest number of coins that we need to make up the amount given.

.
Developed by: Daniel C
Register Number:  212223240023

class Solution(object):
   def coinChange(self, coins, amount):
       
        dp = [float('inf')] * (amount + 1)
        dp[0]=0
        for coin in coins:
            for i in range(coin, amount + 1):
                dp[i] = min(dp[i], dp[i - coin] + 1)
        return dp[amount] if dp[amount]!=float('inf') else -1
      
      
ob1 = Solution()
n=int(input())
s=[]
amt=int(input())
for i in range(n):
    s.append(int(input()))


print(ob1.coinChange(s,amt))
*/
```

## Output:
<img width="945" height="565" alt="image" src="https://github.com/user-attachments/assets/cc6dd6e2-afa1-4a37-83e5-678caf1dddcc" />



## Result:
Thus the program was executed successfully for finding the minimum number of coins required to make amount.
