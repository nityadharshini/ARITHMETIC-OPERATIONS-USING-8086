
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
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| --1200:12 24:1204--------------------- | ------------------------ |
|  1201:34                       | 68:1205
|  1202:12                         00:1206
   1203:14                         c4:1207

#### Manual Calculations
<img width="1196" height="1065" alt="image" src="https://github.com/user-attachments/assets/cfd77fd9-0a32-467f-9072-fcc1c9bb51b1" />

<img width="645" height="416" alt="image" src="https://github.com/user-attachments/assets/f03fc1bd-4c88-4611-a47f-9be60f884a4e" />


## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="631" height="384" alt="image" src="https://github.com/user-attachments/assets/3f656c69-1b76-4c2f-98e7-3dc44a9061ef" />

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
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ---1200:12 24:1204-------------------- | ------------------------ |
|     1201:34                        |       68:1205                   |
      1202:12                                00:1206
      1203:34                                 c4:1207
#### Manual Calculations

<img width="836" height="865" alt="image" src="https://github.com/user-attachments/assets/1a9dd2aa-930a-447b-b3fb-ad6485c33f89" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="552" height="408" alt="image" src="https://github.com/user-attachments/assets/4114e69d-7d20-4ece-b323-6e30831873f6" />
<img width="641" height="431" alt="image" src="https://github.com/user-attachments/assets/23d3523b-1d1a-49b4-b180-57a9247e7d4b" />

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
MOV SI,2000H
MOV DX,0000H
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
| ---1200:12 24:1204-------------------- | ------------------------ |
|    1201:34                       |     68:1205
   1202:12                               00:1206
   1203:34                               c4:1207|

#### Manual Calculations

<img width="580" height="1214" alt="image" src="https://github.com/user-attachments/assets/f1dee1ad-35ec-47cc-9edd-90f1ec0ffcce" />



---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="615" height="395" alt="image" src="https://github.com/user-attachments/assets/2cca44a3-fb6e-40da-816b-58003ff0f5cf" />
<img width="633" height="425" alt="image" src="https://github.com/user-attachments/assets/3b82a324-8cb4-4d0c-b538-6902ffa72ade" />

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
MOV SI,2000H
MOV DX,0000H
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
| --1200:12 24:1204--------------------- | ------------------------ |
|   1201:34                      |    68:1205
    1202:12                           00:1206
    1203:34                           c4:1207|

#### Manual Calculations
<img width="1267" height="969" alt="image" src="https://github.com/user-attachments/assets/25fec864-1137-48d7-aee1-82a577600d3f" />



---
## OUTPUT FROM MASM SOFTWARE
<img width="637" height="402" alt="image" src="https://github.com/user-attachments/assets/83249164-d3b2-4920-abc1-cdce69dbb8a5" />

<img width="637" height="427" alt="image" src="https://github.com/user-attachments/assets/a8e67323-6d4f-412c-b111-d205f1fe9646" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

