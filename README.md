# Workshop
 ### AIM: To design a Verilog module that converts a 4-bit Gray code input into its corresponding 4-bit Binary code output. 
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime 
### Procedure 
Assign the MSB of Binary: binary[3] = gray[3] (The MSB of Binary is the same as the MSB of Gray).

Assign the next bit of Binary: binary[2] = binary[3] ^ gray[2] (XOR the previous Binary bit with the corresponding Gray bit).

Assign the next bit of Binary: binary[1] = binary[2] ^ gray[1].

Assign the least significant bit of Binary: binary[0] = binary[1] ^ gray[0].

### Program
```
module work (
    input [3:0] gray,   
    output [3:0] binary 
);
    assign binary[3] = gray[3]; 
    assign binary[2] = binary[3] ^ gray[2];
    assign binary[1] = binary[2] ^ gray[1];
    assign binary[0] = binary[1] ^ gray[0];

endmodule
```

### output

![Screenshot 2025-05-13 155420](https://github.com/user-attachments/assets/f937eb35-7812-43e0-ba1e-493853432acc)

### Result

thus the Verilog module that converts a 4-bit Gray code input into its corresponding 4-bit Binary code output successfully.

