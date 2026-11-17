# EXPERIMENT-01: BUILDING LOGICAL CIRCUITS

## 1. Aim

To design, implement, simplify, and verify combinational logic circuits using Boolean algebra and digital logic gates.

## 2. Boolean Notation

Use the following notation throughout this experiment:

| Symbol | Meaning | Example |
|---|---|---|
| `!A` | NOT A | `!A` |
| `A & B` | AND | `A & B` |
| `A \| B` | OR | `A \| B` |
| `A ^ B` | XOR | `A ^ B` |
| `A XNOR B` | XNOR | `A XNOR B` |

**Important:** In these equations, `!` means NOT, `&` means AND, `|` means OR, and `^` means XOR. Parentheses determine the order of operations.

## 3. Advanced Boolean Equations

### Equation 1: Four-Input Sum-of-Products

```text
F1 = (!A & B & C)
   | (A & B & !D)
   | (!B & C & D)
   | (A & !C & D)
```

**Inputs:** A, B, C, D  
**Output:** F1  
**Challenge:** Simplify the expression and compare gate counts.

### Equation 2: Product-of-Sums Circuit

```text
F2 = (A | !B | C)
   & (!A | B | D)
   & (B | !C | !D)
```

**Inputs:** A, B, C, D  
**Output:** F2  
**Challenge:** Implement the circuit using NAND gates and verify functional equivalence.

### Equation 3: Nested Complement Logic

```text
F3 = !(
       ((! (A | B)) | (C & D))
       &
       (A | (!(B | C)))
     )
```

**Inputs:** A, B, C, D  
**Output:** F3  
**Challenge:** Apply De Morgan's theorems and implement the circuit using NAND and NOR gates.

### Equation 4: XOR-XNOR Combinational Circuit

```text
F4 = ((A XOR B) & (C XNOR D))
   | (!A & B & (C XOR D))
```

**Inputs:** A, B, C, D  
**Output:** F4  
**Challenge:** Compare an XOR/XNOR implementation with a basic-gate implementation.

### Equation 5: Five-Input Logic Function

```text
F5 = (A & B & !C)
   | (!A & D & E)
   | (B & C & !E)
   | (!B & C & D)
```

**Inputs:** A, B, C, D, E  
**Output:** F5  
**Challenge:** Generate and verify all 32 input combinations.

### Equation 6: Six-Input Mixed Logic

```text
F6 = ((A | B) & !(C | D))
   | ((C XOR E) & (D | G))
   | (!A & B & E)
```

**Inputs:** A, B, C, D, E, G  
**Output:** F6  
**Challenge:** Calculate gate count and logic depth. Verify all 64 input combinations.

### Equation 7: NAND-NOR Hybrid Logic

```text
F7 = (! (A & B) & !(C | D))
   | (!(A | C) & B & D)
```

**Inputs:** A, B, C, D  
**Output:** F7  
**Challenge:** Implement the function using NAND and NOR gates with any required input inversions.

### Equation 8: Six-Input Advanced Combinational Logic

```text
F8 = ((A XOR B) & (C XNOR D))
   | (!(A | B) & C & E)
   | (A & B & !(D | F))
```

**Inputs:** A, B, C, D, E, F  
**Output:** F8  
**Challenge:** Simplify the expression, design the circuit, and verify all 64 input combinations.

## 4. Experimental Procedure

1. Identify all input variables and the output.
2. Draw the logic circuit for each equation.
3. Implement the circuit in Logisim Evolution, Proteus, or a digital logic trainer kit.
4. Apply all possible input combinations.
5. Record the expected and observed outputs.
6. Simplify the Boolean expression using Boolean algebra.
7. Build the simplified circuit and compare gate counts.
8. Save the circuit diagrams, truth tables, and verification screenshots.

## 5. Truth Table Requirements

| Number of inputs | Required combinations |
|---:|---:|
| 4 | 16 |
| 5 | 32 |
| 6 | 64 |

Use this format to record the results:

| Inputs | Expected output | Observed output | Status |
|---|---|---|---|
| 0000 |  |  |  |
| 0001 |  |  |  |
| 0010 |  |  |  |
| ... |  |  |  |

Extend the table to include every input combination required by each equation.

## 6. Performance Analysis

For each circuit, record:

- Number of AND gates
- Number of OR gates
- Number of NOT gates
- Number of XOR/XNOR gates
- Total gate count
- Logic depth
- Functional equivalence before and after simplification

## 7. Expected Results (drop the screenshots of each equations circuit )
F1 = (!A & B & C) | (A & B & !D) | (!B & C & D) | (A & !C & D) Shown with inputs A=0, B=0, C=1, D=1  ->  F1 = 1

F2 = (A | !B | C) & (!A | B | D) & (B | !C | !D) Shown with inputs A=0, B=0, C=0, D=0  ->  F2 = 1

F3 = !( ((!(A | B)) | (C & D)) & (A | (!(B | C))) ) Shown with inputs A=0, B=0, C=1, D=0  ->  F3 = 1

F4 = ((A XOR B) & (C XNOR D)) | (!A & B & (C XOR D)) Shown with inputs A=0, B=1, C=0, D=0  ->  F4 = 1

F5 = (A & B & !C) | (!A & D & E) | (B & C & !E) | (!B & C & D) Shown with inputs A=0, B=0, C=0, D=1, E=1  ->  F5 = 1

F6 = ((A | B) & !(C | D)) | ((C XOR E) & (D | G)) | (!A & B & E) Shown with inputs A=0, B=0, C=0, D=0, E=1, G=1  ->  F6 = 1

F7 = (!(A & B) & !(C | D)) | (!(A | C) & B & D) Shown with inputs A=0, B=0, C=0, D=0  ->  F7 = 1

F8 = ((A XOR B) & (C XNOR D)) | (!(A | B) & C & E) | (A & B & !(D | F)) Shown with inputs A=0, B=0, C=1, D=0, E=1, F=0  ->  F8 = 1

Screenshots:
<img width="773" height="391" alt="image" src="https://github.com/user-attachments/assets/ef676fef-67c5-4852-9391-d0cd4501c6e9" />

<img width="771" height="391" alt="image" src="https://github.com/user-attachments/assets/a3717de2-602b-408d-8a92-0dc7b0438041" />

<img width="767" height="352" alt="image" src="https://github.com/user-attachments/assets/c1323179-317d-4a61-830a-8f8b28ce0dc2" />

<img width="771" height="379" alt="image" src="https://github.com/user-attachments/assets/90dea7e8-cc9a-4602-afca-ccd45b9258a2" />

<img width="769" height="381" alt="image" src="https://github.com/user-attachments/assets/df0fef9d-9520-4ba5-a3c4-e365465126b3" />

<img width="770" height="415" alt="image" src="https://github.com/user-attachments/assets/5f233143-761f-4a34-9c52-4eba02d58704" />

<img width="767" height="427" alt="image" src="https://github.com/user-attachments/assets/b10e5502-85f8-40ea-862a-dd370424581c" />

<img width="769" height="381" alt="image" src="https://github.com/user-attachments/assets/2b2828ad-c416-46f3-ac92-eb5f94f5c752" />










 
## 8. Result

The logic circuits are designed, implemented, and verified using Boolean algebra and digital logic gates. The original and simplified circuits are compared based on gate count and logic depth.
 
 
