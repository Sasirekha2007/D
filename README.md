AIM:

To implement D flipflop using verilog and validating their functionality using their functional tables

SOFTWARE REQUIRED:

Quartus prime

THEORY

D Flip-Flop

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.




<img width="736" height="382" alt="Screenshot 2025-12-14 175657" src="https://github.com/user-attachments/assets/41a230fe-b41f-4bd3-8838-c76f9790cf03" />



This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.


<img width="510" height="205" alt="Screenshot 2025-12-14 175708" src="https://github.com/user-attachments/assets/443cf7dd-8a7a-4315-81f5-e3ac1eb4e9a5" />


Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D



<img width="460" height="273" alt="Screenshot 2025-12-14 175723" src="https://github.com/user-attachments/assets/beaaf921-c8ed-4778-902b-601ec6850c72" />


Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.



PROGRAM

module D (
    input  wire clk, rst, D,
    output reg  Q
);
    always @(posedge clk or posedge rst) begin
        if (rst)
            Q <= 1'b0;   // Reset
        else
            Q <= D;      // Capture D at clock edge
    end
endmodule


Developed by: B.SASIREKHA

RegisterNumber: 25015734

RTL LOGIC FOR FLIPFLOPS

TIMING DIGRAMS FOR FLIP FLOPS

RESULTS
