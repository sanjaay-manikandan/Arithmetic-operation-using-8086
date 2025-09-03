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

| MEMORY LOCATION (INPUT)       | MEMORY LOCATION (OUTPUT) |
| -----------------------       | ------------------------ |
|          1200:  12            | 1204: 24                 |
|          1201:  34            | 1205: 68                 |
|          1202:  12            | 1206: 00                 |
|          1203:  34            |                          |
____________________________________________________________
#### Manual Calculations

![Addn](https://github.com/user-attachments/assets/bbd65838-303c-460a-83d3-d8da237aca1c)


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="1043" height="633" alt="image" src="https://github.com/user-attachments/assets/204e3965-e38c-4eab-bfac-36b61ce599cd" />
<img width="940" height="705" alt="image" src="https://github.com/user-attachments/assets/791a5a11-6173-4a89-9a58-bdd06eeee4c6" />




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



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|        1200:12          | 1204:00                  |
|        1201:34          | 1205:00                  |
|        1202:12          | 1206:00                  |
|        1203:34          |                          | 
______________________________________________________

#### Manual Calculations

![sub](https://github.com/user-attachments/assets/3f6dbabf-9576-48fb-b135-9edbd3eca373)

---
## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="940" height="705" alt="image" src="https://github.com/user-attachments/assets/ccbd596e-74e6-4514-bbbb-7670f88c0a76" />
<img width="940" height="705" alt="image" src="https://github.com/user-attachments/assets/cb04601f-85a2-4a6d-89a8-546510f3bd32" />



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
| ----------------------- | ------------------------ |
|  1200:12                | 1204:44                  |
|  1201:34                | 1205:51                  |
|  1202:12                | 1206:97                  |
|  1203:34                |                          |
______________________________________________________
#### Manual Calculations

![mul](https://github.com/user-attachments/assets/582c7d76-d98a-41a4-8e9f-dc3cd2bd7826)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="940" height="705" alt="image" src="https://github.com/user-attachments/assets/472fad65-c247-4b2c-86b5-e8be1b4a7163" />
<img width="940" height="705" alt="image" src="https://github.com/user-attachments/assets/7005bc12-8945-49d3-9232-55ce195e5576" />




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
| ----------------------- | ------------------------ |
| 1200:12                 | 1204: 01                 |
| 1201:34                 | 1205: 00                 |
| 1202:12                 | 1206: 00                 |
| 1203:34                 |                          |
______________________________________________________
#### Manual Calculations

![div](https://github.com/user-attachments/assets/fc691346-f5d4-4901-aaec-c2505efdf5b6)


---
## OUTPUT FROM MASM SOFTWARE
<img width="940" height="705" alt="image" src="https://github.com/user-attachments/assets/42d77184-0756-4f14-bf42-847c774fabc1" />
<img width="940" height="705" alt="image" src="https://github.com/user-attachments/assets/e2dec1dc-b7dd-4dee-af83-2f1ff38831d6" />





## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
