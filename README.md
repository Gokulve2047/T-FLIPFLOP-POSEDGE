**AIM:**

To implement  T flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**T Flip-Flop**

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/458a68fe-2d08-4a9d-ac4f-7ae0480ce0bd)

 
This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/cdd7fb32-539f-4b66-bb8d-f305a153c886)

 
From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

**Procedure**

/* write all the steps invloved */

**PROGRAM**
```
/* Program for flipflops and verify its truth table in quartus using Verilog programming.
Developed by:GOKUL V E
RegisterNumber:24002047
*/
```

```
module t_flipflop (
    input clk,    // Clock signal
    input reset,  // Active-high reset
    input t,      // Toggle input
    output reg q  // Output
);
    always @(posedge clk or posedge reset) begin
        if (reset)
            q <= 1'b0; // Reset output to 0
        else if (t)
            q <= ~q; // Toggle output
    end
endmodule
```
**RTL LOGIC FOR FLIPFLOPS**
![Screenshot 2024-12-27 211712](https://github.com/user-attachments/assets/4c1ccd8f-6762-4c75-97ac-b242bd2e169f)


**TIMING DIGRAMS FOR FLIP FLOPS**
![Screenshot 2024-12-27 211725](https://github.com/user-attachments/assets/2f4fb3c2-e7cf-4f72-8eac-e74dcfeec044)


**RESULTS**
The observation of the stimulation results and confirm the successful execution of the program.
