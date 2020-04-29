# Append-and-Delete
#!/bin/python3

import math
import os
import random
import re
import sys

# Complete the appendAndDelete function below.
def isConvertible(str1, str2, k): 
      
    # Case A (i) 
    if ((len(str1) + len(str2)) < k): 
        return True
  
    # finding common length of both string 
    commonLength = 0
    for i in range(0, min(len(str1),  
                          len(str2)), 1): 
        if (str1[i] == str2[i]): 
            commonLength += 1
        else: 
            break
  
    # Case A (ii)- 
    if ((k - len(str1) - len(str2) + 2 * 
                commonLength) % 2 == 0): 
        return True
  
    # Case B- 
    return False
  
# Driver Code 
if __name__ == '__main__': 
    str1 =input()
    str2 =input()
    k =int(input())
    if (isConvertible(str1, str2, k)): 
        print("Yes") 
    else: 
        print("No") 
  
    
