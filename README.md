
#  2-Bit Arithmetic Logic Unit (ALU) – Digital Logic Design

##  Overview
This project implements a **2-bit Arithmetic Logic Unit (ALU)** using **digital logic circuits**, designed and simulated in **Proteus** and physically implemented on a breadboard.

The ALU is capable of performing both:
-  Arithmetic operations (Addition & Subtraction)  
-  Logical operations (AND, OR, NOT)  

This project demonstrates core concepts in **digital electronics, combinational logic design, and circuit simulation**.

> The system combines multiple digital components such as full adders, logic gates, and multiplexers to perform different operations :contentReference[oaicite:0]{index=0}.

---

##  Features

-  2-bit Addition (Full Adder)  
-  2-bit Subtraction (Full Subtractor)  
-  Logical AND operation  
-  Logical OR operation  
-  NOT operation (bit inversion)  
-  Operation selection using **Multiplexer (MUX)**  
-  Simulation in Proteus  
-  Physical hardware implementation (breadboard)  

---

##  System Design

###  Core Components

The ALU is built using:

- **Full Adder**
- **Full Subtractor**
- **Logic Gates** (AND, OR, NOT, XOR)
- **4×1 Multiplexer (74153 IC)**

> The multiplexer selects which operation output is sent to the final output based on control signals :contentReference[oaicite:1]{index=1}.

---

###  Operation Selection

The ALU uses **2 selector bits (S1, S0)**:

| S1 | S0 | Operation |
|----|----|----------|
| 0  | 0  | NOT      |
| 0  | 1  | Subtraction |
| 1  | 0  | AND / OR |
| 1  | 1  | Addition |

---

###  Full Adder Logic

- Inputs: `A`, `B`, `Cin`  
- Outputs: `Sum`, `Carry`  

Built using:
- 2 XOR gates  
- 2 AND gates  
- 1 OR gate  

> As explained in the report (page 3), the sum and carry are derived from XOR and AND/OR combinations :contentReference[oaicite:2]{index=2}.

---

###  Multiplexer (MUX)

- 4 input lines (I0–I3)  
- 2 selector lines (S0, S1)  
- 1 output  

Controls which operation result is forwarded to output

---

##  Simulation (Proteus)

Below is the Proteus simulation of the ALU circuit:

![ALU Proteus Simulation](assets/alu-proteus.png)


> The simulation (also shown in the report page 7) demonstrates correct behavior of logic gates and operation switching :contentReference[oaicite:4]{index=4}.

---

##  Hardware Implementation

The circuit was also implemented physically using a breadboard


> Real hardware implementation confirms the correctness of the design beyond simulation :contentReference[oaicite:6]{index=6}.

---

##  How It Works

1. Input bits (A, B) are provided  
2. All operations are computed in parallel:
   - Adder  
   - Subtractor  
   - Logic gates  
3. Multiplexer selects output based on control signals  
4. Final result is displayed  

---

##  Technologies Used

- **Digital Logic Design**
- **Proteus Simulation**
- **Logic ICs (74153, XOR, AND, OR, NOT)**
- **Breadboard Hardware Implementation**

---

##  Project Structure

```

project/
│── Digital Project Report.pdf
│── circuit.pdf
│── README.md

```

---

##  Project Documentation

 Full report available here:  
[View Report](Digital Project Report.pdf)

---

##  What I Learned

- Designing combinational circuits  
- Building full adder and subtractor circuits  
- Using multiplexers for control logic  
- Simulating circuits using Proteus  
- Translating simulation into real hardware  
- Debugging hardware wiring  

---

##  Limitations

- Limited to 2-bit operations  
- No clock or sequential logic  
- Manual input/output  

---

##  Future Improvements

- Expand to 4-bit or 8-bit ALU  
- Add shift operations  
- Integrate with microcontroller  
- Add display (7-segment / LCD)  
- Implement FPGA version  

---

##  Author

**Laila Tarek**
```

