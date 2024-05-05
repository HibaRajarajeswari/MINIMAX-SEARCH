# Lab Experiment 3: Minimaxsearch
## DATE : 24/02/24
## REGISTER NUMBER:212221040056
# AIM
## Write a program to implement minimax search and find optimal value obtianed by root node .
# PROGRAM
```
import math
def minimax (curDepth, nodeIndex, maxTurn, scores,targetDepth):
    # base case : targetDepth reached
    if (curDepth == targetDepth):
        return scores[nodeIndex]
    if (maxTurn):
        return max(minimax(curDepth + 1, nodeIndex * 2,False, scores, targetDepth),
                   minimax(curDepth + 1, nodeIndex * 2 + 1,
                    False, scores, targetDepth))
     
    else:
        return min(minimax(curDepth + 1, nodeIndex * 2, True, scores, targetDepth),
                   minimax(curDepth + 1, nodeIndex * 2 + 1,
                     True, scores, targetDepth))
     
# Driver code
scores = [3, 5, 2, 9, 12, 5, 23, 20]
treeDepth = math.log(len(scores), 2) # calculate depth of node  log 8 (base 2) = 3)
print("The optimal value is : ", end = "")
print(minimax(0, 0, True, scores, treeDepth))
```
# OUTPUT
![image](https://github.com/HibaRajarajeswari/MINIMAX-SEARCH/assets/129970809/7785d48c-8afd-4a61-993e-6a592c9409bf)

# RESULT
A program to implement minimax search and find optimal value obtianed by root node is implemented
