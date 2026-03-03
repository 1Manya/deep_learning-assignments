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

 - Layer 1: 8*3 + 8 = 32
 - Layers 2-8 (7 layers): 7 * (8*8+8) = 7 * 72 = 504
 - Output:  1*8 + 1 = 9
 - **TOTAL = 545**

---
##  Observation Table

[Click here to view Observation Table](observation_table.csv)

---
##  Reflections 
Q1. Did deeper always reduce loss faster?
- No. Looking at my results, 
- Model A actually had the lowest final loss of 0.39, while deeper models like C and D had much higher losses around 1.88 and 1.94.
-  So going deeper did not help.

Q2. Did gradients in early layers stay similar to later layers?
- No, they were different. For ex. 
- in Model D with ReLU, the gradient norm at layer 1 was 7.07e-07 and at the last hidden layer it was 5.79e-07  both almost zero. 
- In Model B, layer 1 had 0.335 and last layer had 0.512
- there was a clear difference between early and late layers.

Q3. Was training equally stable for all activations?
- No. Model D with ReLU had a final loss of 1.946 and Model D with Sigmoid also had 1.946 — both were very high and barely improved. Compared to Model A which reached 0.39, the deeper models with both activations were clearly struggling and unstable.

Q4. Which activation behaved more stable in deeper networks?
- Both behaved poorly in the very deep network (Model D), but ReLU was slightly better.

Q5. Did some models improve very slowly even though learning rate was same?
- Yes, Model D improved very slowly because its layer 1 gradient was almost zero (7e-07), so weights barely updated regardless of learning rate.

---
