# Huffman-Shannon_fano
# Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. Apply the Huffman and Shannon-Fano to this source. Show that draw the tree diagram, the average code word length, Entropy, Variance, Redundancy, Efficiency.
# Aim:
To compute the Average Codeword Length, Entropy, Efficiency, Redundancy, and Variance
for a discrete memoryless source using Huffman and Shannon-Fano coding based on the
given probabilities and codeword lengths.

# Tools Required:
Python: A versatile language for scientific computing and signal processing.
NumPy & Matplotlib: Libraries for numerical operations and high-quality visualizations,
essential for demonstrating sampling.
# Program:
```
import numpy as np
import math
L = 0
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
eff = hs / L
eff = round(eff,3)
red = round(1 - eff,3)
var = 0
for k in range(n):
var1 = p[k] * (lk[k]-L)**2
var = var + var1
var = round(var,3)
print()
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff*100} %")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```
# Output:
![image](https://github.com/user-attachments/assets/45d9d15b-44d6-4bd4-946c-083c72968e3f)

# Calculation:
![image](https://github.com/user-attachments/assets/33e5fa1b-80b8-4cbc-9ee4-2423dadfb8bd)
![image](https://github.com/user-attachments/assets/63d3b923-7765-4729-9a26-47093c17ffa1)
![image](https://github.com/user-attachments/assets/cae690d2-5753-4e02-b9bc-a73e4b3f7be8)

# Results:
For the given probabilities 0.125,0.0625,0.25,0.0625,0.125,0.125,0.25.
Average Codeword Length is : 2.625
Entropy is : 2.625
Efficiency is : 100.0 %
Redudancy is : 0.0
Variance is : 0.484.
