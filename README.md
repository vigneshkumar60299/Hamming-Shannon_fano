# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
# Program:
```
import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)

for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1

for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)

eff =  hs / L
eff = round(eff,3)
red =  round(1 - eff,3) 

var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```
# Calculation:

<img width="771" height="1280" alt="484085350-17ddac48-1f60-4992-b789-681f5465a5a7" src="https://github.com/user-attachments/assets/d1c24f39-efb9-4c75-a52f-eb1066748b61" />


<img width="771" height="1280" alt="484085350-17ddac48-1f60-4992-b789-681f5465a5a7" src="https://github.com/user-attachments/assets/fc597ebb-b4c5-422a-8411-de004f4873e1" />




# Output

<img width="455" height="360" alt="Screenshot 2026-05-22 155424" src="https://github.com/user-attachments/assets/b423240c-68a1-4913-aa95-fdd7b3b1b39d" />


# Results:
The Huffman and Shannon-Fano of the given statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} using python are verified.
