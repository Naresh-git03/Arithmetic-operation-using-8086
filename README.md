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
| ----------------------- | ------------------------ |
|<img width="640" height="480" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/11ccedab-74aa-46e5-ac42-68bffe93d6f3" />|<img width="640" height="480" alt="Screenshot (7)" src="https://github.com/user-attachments/assets/cb528ee9-c0cf-4987-9bbc-7886f95a74a9" />|

#### Manual Calculations

|![IMG-20250901-WA0019](https://github.com/user-attachments/assets/bcfe02ad-8dac-490d-bd79-7e2d9a01090a)|


---

## OUTPUT IMAGE FROM MASM SOFTWARE

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
|<img width="640" height="480" alt="Screenshot (10)" src="https://github.com/user-attachments/assets/4041575d-48de-48b3-802b-a9f10b7cbc01" />|<img width="640" height="480" alt="Screenshot (11)" src="https://github.com/user-attachments/assets/42446b8e-5577-4a81-8e7b-a0590e66fde3" />|

#### Manual Calculations

|![IMG-20250901-WA0018](https://github.com/user-attachments/assets/0196abb1-125a-4511-9f9f-2429f34a0a3f)|

---


## OUTPUT SCREEN FROM MASM SOFTWARE

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
|<img width="640" height="480" alt="Screenshot (13)" src="https://github.com/user-attachments/assets/67bf4dcc-4931-4ceb-8362-16f3a0c412d7" />|<img width="640" height="480" alt="Screenshot (12)" src="https://github.com/user-attachments/assets/2c885f8f-ad1b-42c1-b73b-704dd41e9a24" />|

#### Manual Calculations

|![IMG-20250901-WA0013](https://github.com/user-attachments/assets/7ad22ff1-de4e-4b8d-9877-9d47579bf2b8)|


---

## OUTPUT SCREEN FROM MASM SOFTWARE

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
|<img width="640" height="480" alt="Screenshot (15)" src="https://github.com/user-attachments/assets/2b722ad0-6bdc-491b-b36b-3a319a60c4e8" />|<img width="640" height="480" alt="Screenshot (14)" src="https://github.com/user-attachments/assets/2926f570-6e4a-417a-8f6a-038fc6b0d9ce" />|

#### Manual Calculations

|![IMG-20250901-WA0017](https://github.com/user-attachments/assets/e43044c3-a5f6-46ab-b84a-01ef04a5ae2e)|


---
## OUTPUT FROM MASM SOFTWARE



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
