# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
1.Computer with i3 processor
2.Python Colab
# Theory:
Huffman coding is an optimal lossless compression algorithm that constructs codes based on symbol probabilities using a binary tree. It is widely used in digital communication systems for efficient data transmission.

Shannon–Fano coding is a lossless data compression technique used in digital communication to reduce the number of bits required to represent data. It assigns shorter codes to symbols with higher probability and longer codes to symbols with lower probability.
# Program:
```
#Huffman and Shannon-Fano coding
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
Write the program 
```
# Calculation:

![WhatsApp Image 2026-02-09 at 6 28 30 PM (1)](https://github.com/user-attachments/assets/77812068-8ee4-4df6-ad3d-63d63d6f5581)


![WhatsApp Image 2026-02-09 at 6 28 30 PM](https://github.com/user-attachments/assets/338dfbd1-b85c-4a56-9c3e-644fdd616f8f)

Compare the manually calculated value and the observed practical value.

# Output

<img width="513" height="288" alt="Screenshot (158)" src="https://github.com/user-attachments/assets/7720a6c6-491c-47b6-aea4-47060beb90a5" />


# Results:
```
Thus, the python program for Huffman-Shannon_fano has been executed and verified successfully.
```
