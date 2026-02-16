# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
colab/jupyter
# Program:
```
import math

n = int(input("Enter number of samples: "))
p  = [float(input(f"P{i+1}: ")) for i in range(n)]
lk = [float(input(f"L{i+1}: ")) for i in range(n)]

L  = sum(p[i]*lk[i] for i in range(n))                     # Avg length
hs = round(sum(p[i]*math.log2(1/p[i]) for i in range(n)),3) # Entropy
eff = round(hs/L,3)                                        # Efficiency
red = round(1-eff,3)                                       # Redundancy
var = round(sum(p[i]*(lk[i]-L)**2 for i in range(n)),3)    # Variance

print("Average Length:", L)
print("Entropy:", hs)
print("Efficiency:", eff)
print("Redundancy:", red)
print("Variance:", var)
```
# Calculation:
<img width="900" height="1000" alt="image" src="https://github.com/user-attachments/assets/492e0d3a-d825-4b2e-a362-0de413dcac91" />

<img width="900" height="1000" alt="image" src="https://github.com/user-attachments/assets/cac7622a-0913-4b4b-a55e-40167507df80" />
<img width="900" height="200" alt="image" src="https://github.com/user-attachments/assets/4c05d200-398a-4dd2-8474-d9dbfc97c6d0" />



# Output
<img width="400" height="150" alt="image" src="https://github.com/user-attachments/assets/f2e7d611-04d0-456d-966c-85b97542b5f7" />
 
# Results:
```
Write the conclusion
```
