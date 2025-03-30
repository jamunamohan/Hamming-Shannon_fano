Exp-8: Huffman-Shannon_fano
Name: Jamuna M
Reg No.: 212223060097

Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output.
Apply the Huffman and Shannon-Fano to this source. Show that draw the tree diagram, the average code word length, Entropy, Variance, Redundancy, Efficiency.

Aim :

To compute the Average Codeword Length, Entropy, Efficiency, Redundancy, and Variance for a discrete memoryless source using Huffman and Shannon-Fano coding based on the given probabilities and codeword lengths.

Tools Required :

Python IDE with

-> numpy library

-> math library

Program :

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
# Avg length of the code word
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
# Entropy
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
# Efficiency
eff =  hs / L
eff = round(eff,3)
# Redundancy 
red =  round(1 - eff,3) 
# Variance
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

Calculation :

![image](https://github.com/user-attachments/assets/9e1f0d45-2e5f-44d7-88ae-3ceb35537ef0)
![image](https://github.com/user-attachments/assets/78641127-62e1-40de-8ce8-4a675858099a)
![image](https://github.com/user-attachments/assets/68e1ce08-8cb2-4adb-a4d8-e3e9a3c1392a)
![image](https://github.com/user-attachments/assets/0f310b8c-ec09-47b2-9046-a881a034ef01)
![image](https://github.com/user-attachments/assets/0b7440b5-4f02-4a48-8570-84c828171e8d)

Results :

The obtained result are

Average Codeword Length is : 2.625

Entropy is : 2.625

Efficiency is : 1.0

Redudancy is : 0.0

Variance is : 0.484

