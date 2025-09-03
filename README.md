# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,1200H
MOV AX,[SI]
MOV BX,[SI+02H]
MOV CL,00H
ADD AX,BX
JNC L1
INC CL
L1:MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 1200=12                 | 1204=24              
| 1201=34                 | 1205=68
| 1202=12                 |
| 1203=34                 |

#### Manual Calculations

(![WhatsApp Image 2025-09-03 at 08 55 03_ed3e9259](https://github.com/user-attachments/assets/759e752b-9684-4e29-b5aa-67e15f18efef)
Add your calculation here)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (6)" src="https://github.com/user-attachments/assets/832149bc-fb63-441e-9211-5a6440d366dd" />

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
<img width="640" height="480" alt="Screenshot (21)" src="https://github.com/user-attachments/assets/cdb27271-5cbc-48dd-9fdf-c77e97e6515f" />


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 1200=12                 |  1204=00
| 1201=34                 |  1205=00
| 1202=12
|  1203=34

#### Manual Calculations

(![WhatsApp Image 2025-09-03 at 08 55 03_952c8a93](https://github.com/user-attachments/assets/d421817d-bacd-4f73-83fb-e8437b78892c)
Add your calculation here)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/bac91bbf-f6ef-4ce5-93b0-abe81003eb36" />

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,1200H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  1200=12                |  1204=44
|  1201=34                |  1205=51
|  1202=12                |  1206=97
|  1204=34                |  1207=0

#### Manual Calculations

(![WhatsApp Image 2025-09-03 at 08 55 02_b8e8ac01](https://github.com/user-attachments/assets/c9e9f9c4-2c0d-4dd0-bace-512f055e2d4c)
Add your calculation here)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/0d14e58d-6b44-4d22-8895-b3a94d887743" />

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,1200H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  1200=12                |   1204=01
|  1201=34                |   1205=00
|  1202=12                |
   1203=34                |      

#### Manual Calculations

(![WhatsApp Image 2025-09-03 at 08 55 02_041b9ef9](https://github.com/user-attachments/assets/87bb6233-d054-4089-b077-d801c00db1c0)
Add your calculation here)

---
## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2025-09-03 at 08 55 18_5efc08af](https://github.com/user-attachments/assets/fb308278-265c-41ec-aa00-2b0871b7c3f6)



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
