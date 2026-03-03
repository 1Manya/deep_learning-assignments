# Parameter Counting

**Formula:**  
Parameters in a layer = (neurons_out × neurons_in) + neurons_out

---

## Model A: 3 → 4 → 1

- Layer 1: 4 × 3 + 4 = 16
- Output Layer: 1 × 4 + 1 = 5
- **TOTAL = 21**

---

## Model B: 3 → 6 → 6 → 4 → 1

- Layer 1: 6 × 3 + 6 = 24
- Layer 2: 6 × 6 + 6 = 42
- Layer 3: 4 × 6 + 4 = 28
- Output Layer: 1 × 4 + 1 = 5
- **TOTAL = 99**

---

## Model C: 3 → 8 → 8 → 8 → 8 → 1

- Layer 1: 8 × 3 + 8 = 32
- Layer 2: 8 × 8 + 8 = 72
- Layer 3: 8 × 8 + 8 = 72
- Layer 4: 8 × 8 + 8 = 72
- Output Layer: 1 × 8 + 1 = 9
- **TOTAL = 257**
---

## Model D:  3 --> 8 --> 8 --> 8 --> 8 --> 8 --> 8 --> 8 --> 8 --> 1
   -Layer 1: 8*3 + 8 = 32
   -Layers 2-8 (7 layers): 7 * (8*8+8) = 7 * 72 = 504
   -Output:  1*8 + 1 = 9
   -**TOTAL = 545**

---

