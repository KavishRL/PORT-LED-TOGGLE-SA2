# PORT-LED-TOGGLE-SA2
SKILL ASSIGNMENT-2

NAME: KAVISH RAJESHKUMAR

REGNO: 212224060120

PROGRAM: Write an assembly language program in 8051 to generate a 50 ms delay using Timer 0 in Mode 2 (8-bit auto-reload mode) and blink an LED connected to Port 3.0.

APPARATUS REQUIRED:

LAPTOP WITH KEIL SOFTWARE

PROGRAM:
```
ORG 0H         

MOV P3, #00H    

MOV TMOD, #02H  
MOV TH0, #56H
MOV TL0, #56H   

SETB TR0        

MAIN:
    MOV R2, #250   

WAIT_OVERFLOW:
    JNB TF0, $     
    CLR TF0        
    DJNZ R2, WAIT_OVERFLOW 

    CPL P3.0       
    SJMP MAIN      

END
```
OUTPUT:
<img width="962" height="786" alt="image" src="https://github.com/user-attachments/assets/6f58bf42-6ab0-4f75-b09b-111db8ee23ce" />

RESULT:
Thus the assembly language program in 8051 to generate a 50 ms delay using Timer 0 in Mode 2 (8-bit auto-reload mode) and blink an LED connected to Port 3.0 is created and executed succesfully.
