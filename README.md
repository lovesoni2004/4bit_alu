# 4-Bit ALU (Arithmetic Logic Unit) in Verilog

This project implements a 4-bit Arithmetic Logic Unit (ALU) in Verilog, capable of performing basic arithmetic and logic operations such as addition, subtraction, AND, OR, and XOR. It also includes a testbench to simulate and verify the ALU's functionality using ModelSim or any other Verilog simulator.

---

##  Features

- 4-bit inputs `A` and `B`
- 3-bit control input `OP` to select operation
- 4-bit output `Result`
- Supported operations:
  - `000`: Addition (`A + B`)
  - `001`: Subtraction (`A - B`)
  - `010`: Bitwise AND (`A & B`)
  - `011`: Bitwise OR (`A | B`)
  - `100`: Bitwise XOR (`A ^ B`)

---

##  File Structure

```
4bit-ALU-Verilog/
│
├── ALU_4bit.v             # Main ALU module
├── testbench_ALU.v        # Testbench for simulating ALU behavior
└── README.md              # Project documentation (you are here)
```

---

##  Getting Started

### Requirements
- Any Verilog simulator (e.g., ModelSim, Icarus Verilog, XSIM, etc.)


### Running the Simulation (ModelSim Example)

1. **Open ModelSim.**
2. **Compile** the design:
   ```bash
   vlog ALU_4bit.v testbench_ALU.v
   ```
3. **Simulate** the testbench:
   ```bash
   vsim testbench_ALU
   ```
4. **View output** in the transcript/log.


---

## 📊 Sample Output

```
Time    A     B     OP    Result
-------------------------------
1       0010  0101  000   0111
11      0101  0010  001   0011
21      1100  1010  010   1000
31      1100  1010  011   1110
41      1100  1010  100   0110
```

---

##  Test Cases

| A (hex) | B (hex) | OP Code | Operation | Result |
|---------|---------|---------|-----------|--------|
| 0x2     | 0x5     | 000     | ADD       | 0x7    |
| 0x5     | 0x2     | 001     | SUB       | 0x3    |
| 0xC     | 0xA     | 010     | AND       | 0x8    |
| 0xC     | 0xA     | 011     | OR        | 0xE    |
| 0xC     | 0xA     | 100     | XOR       | 0x6    |

---



## License

This project is open-source. Feel free to modify and use it for educational or personal purposes.

---

##  Author

Developed by Love Soni  
B.Tech Electronics & Communication Engineering  
VIT University
