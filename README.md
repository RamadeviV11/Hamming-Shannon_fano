# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.4, 0.19, 0.16, 0.15, 0.15} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:

Google colab

# Program:
```
import math

p = [0.4, 0.19, 0.16, 0.15, 0.15]
lk = [3, 4, 2, 4, 3, 3, 2]
n = len(p)

L = sum(p[k] * lk[k] for k in range(n))
hs = sum(p[k] * math.log(1 / p[k], 2) for k in range(n))
hs = round(hs, 3)

eff = round(hs / L, 3)
red = round(1 - eff, 3)

var = sum(p[k] * (lk[k] - L) ** 2 for k in range(n))
var = round(var, 3)

print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")


```
# Calculation:
<img width="966" height="1600" alt="image" src="https://github.com/user-attachments/assets/266327e1-ff5c-4ebb-bee9-46bcf210f906" />
<img width="800" height="1328" alt="image" src="https://github.com/user-attachments/assets/baa304a8-245c-49bf-b7dc-26e1e08d6f4b" />

# Output
<img width="477" height="108" alt="image" src="https://github.com/user-attachments/assets/739f75c6-b112-4e4a-a302-f5a4d1715948" />

# Results:
The Huffman and Shannon-Fano of the given statistics {0.4, 0.19, 0.16, 0.15, 0.15} using python are verified.
