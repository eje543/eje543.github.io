```mermaid
  graph TD
    A(((Pick A Number 1-10))) ==Correct==> B(((That's it, you're right!)))
    A --Too Low--> D(Choose a higher number)
    A --Too High--> E(Choose a lower number)
    A --Alphanumeric data or decimal--> C{No letters or decimals. Pick a whole number 1-10}
    A --Not in range--> F{Number must be between 1-10}
        F ==Correct==> B
        F --Alphanumeric data or decimal--> C
        F --Too Low--> D
        F --Too High--> E
    C ==Correct==> B
        C --Too High--> E
        C --Too Low--> D
    E ==Correct==> B
        E -.Too Low.-> D
        E -.Too High.-> E
    D ==Correct==> B
        D -.Too High.-> E
        D -.Too Low.-> D
   
```

*A*) Starts the game  
*B*) If guess is correct, the game ends  
*C*) If a letter or decimal is entered, asks player to enter a whole number 1-10  
*D*) If guess is too low, choose a higher number  
*E*) If guess is too high, choose a lower number  
*F*) If guess is a number not in range, choose a number in range  
