
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
 MEMORY LOCATION (INPUT)|	MEMORY LOCATION (OUTPUT)
 1200:12                 | 1204:24
 1201:34                 | 1205:68
 1202:12                 |  
 1203:34                 |
 


#### Manual Calculations
![WhatsApp Image 2025-11-11 at 19 23 47_023a2e7f](https://github.com/user-attachments/assets/d0505a62-dc55-4846-9101-fc07dc914367)


## output image
<img width="692" height="430" alt="484579792-a49b6d47-653d-4b81-873c-ef4f010a395e" src="https://github.com/user-attachments/assets/08bf836e-f50f-4f7d-9a3a-fa9dd2878cf9" />
<img width="692" height="329" alt="484578699-65510bee-afd9-4eb5-b9d3-232f98cea4c5" src="https://github.com/user-attachments/assets/a48ec2e2-24b4-41f9-873a-90256e257082" />

## 2. Subtraction

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
 MEMORY LOCATION (INPUT)|	MEMORY LOCATION (OUTPUT)
 
 1200:12                |	1204:00
 1201:34                |	1205:00
 1202:12	              |
 1203:34                |

#### Manual Calculations
![WhatsApp Image 2025-11-11 at 19 30 28_3688626d](https://github.com/user-attachments/assets/62e79901-b56b-4f1c-b881-b214a84a7abd)



---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="692" height="431" alt="484579662-bcfa01c8-2f73-4d25-89c2-f34a5e7a8e49" src="https://github.com/user-attachments/assets/0ca1e2d0-00d8-4926-b6e5-5b985a1db97c" />
<img width="692" height="440" alt="484578775-37d7802e-55a4-42ec-b9c7-21ac111aa7c2" src="https://github.com/user-attachments/assets/a5250a8e-7a7a-4bee-8218-946513f546b7" />

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
MEMORY LOCATION (INPUT)|	MEMORY LOCATION (OUTPUT)

 1200:12                |	1204:44
 1201:34	              |   1205:51
 1202:12                |	1206:97
 1203:34                |	1207:0A

#### Manual Calculations

![WhatsApp Image 2025-11-11 at 19 33 06_6c5554be](https://github.com/user-attachments/assets/ec5a4ae1-6837-4574-b8bc-3e2b46327b5a)


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="692" height="435" alt="484579575-4e2dca42-adb7-4e97-96cf-96c279585cd5" src="https://github.com/user-attachments/assets/90d89350-7e2d-494f-ae05-54e81227769b" />
<img width="692" height="444" alt="484578856-5364011b-6bcb-4a2f-8b2e-acde4a2181f2" src="https://github.com/user-attachments/assets/7927d95a-5fcd-4830-9906-525fca2069c9" />

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
MEMORY LOCATION (INPUT)|	MEMORY LOCATION (OUTPUT)

 1200:12	              | 1204:01
 1201:34	              | 1205:00
 1202:12	              | 1206:00
 1203:34	              |

#### Manual Calculations
![WhatsApp Image 2025-11-11 at 19 36 10_9e9d3e0b](https://github.com/user-attachments/assets/0234e17e-20eb-4a26-9456-7311a096ca89)

## OUTPUT FROM MASM SOFTWARE
<img width="692" height="434" alt="484579474-f89d2c67-e1c1-4cb2-9f4e-e32fc3bb72f4" src="https://github.com/user-attachments/assets/c2f90d2b-fc4e-4700-8cc4-18563e41b04f" />
<img width="692" height="435" alt="484579002-b03e0dc7-d966-4cba-a749-2267e27dc70c" src="https://github.com/user-attachments/assets/5ea6fb28-f8a5-41d8-8c4f-adf3f7a15a23" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

