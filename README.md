
# **Functional Verification of FIFO Using SystemVerilog**

## **Overview**
This project demonstrates the functional verification of a FIFO (First-In, First-Out) buffer using SystemVerilog. The verification environment employs advanced verification techniques such as mailbox-based communication, scoreboarding, and constrained random stimulus to validate the FIFO design.



## **Features**
- **SystemVerilog Testbench** with object-oriented programming concepts.
- **Mailbox-Based Communication** for synchronizing data transactions between components.
- **Scoreboarding Mechanism** for result checking and ensuring data integrity.
- **Constrained Random Stimulus** to generate varied test scenarios.
- **Self-Checking Testbench** detects mismatches and logs errors automatically.

## **Project Structure**
| Module         | Description                          |
|----------------|--------------------------------------|
| FIFO.sv        | FIFO Design Implementation           |
| tb.sv          | SystemVerilog Testbench              |
| transaction    | Defines transaction-level stimulus   |
| generator      | Generates input stimulus             |
| driver         | Drives transactions to the FIFO DUT  |
| monitor        | Observes DUT signals and logs data   |
| scoreboard     | Compares expected vs. actual results |
| environment    | Connects all verification components |
| interface      | Defines FIFO interface signals       |


## **Verification Methodology**

### **Mailbox**
- A mailbox is used for inter-process communication between different verification components. It enables transaction-level communication, allowing the generator to send randomized transactions to the driver and ensuring synchronized execution between the components.

### **Scoreboarding**
- The scoreboard is responsible for comparing expected outputs with actual DUT outputs. It maintains a reference queue that tracks written data and checks whether the data read from the FIFO matches expectations, reporting mismatches as errors.

## **Technologies Used**
- **SystemVerilog**: For writing the verification testbench.
- **Mailbox**: Used for communication between components in the testbench.
- **Scoreboarding**: To validate FIFO functionality by maintaining expected outputs.
- **Vivado Simulator**: Used for running the testbench and verifying FIFO behavior.

## **Results & Observations**

- Successfully verified FIFO functionality with randomized stimuli.
- Used scoreboarding to compare expected and actual outputs.
- Identified potential corner cases for further testing.

### **TCL console**

![App Screenshot](https://github.com/itsharshschoice/Functional-Verification-of-FIFO-Using-SystemVerilog/blob/main/Screenshots/TCL_Console_1.png?raw=true)

![App Screenshot](https://github.com/itsharshschoice/Functional-Verification-of-FIFO-Using-SystemVerilog/blob/main/Screenshots/TCL_Console_2.png?raw=true)

![App Screenshot](https://github.com/itsharshschoice/Functional-Verification-of-FIFO-Using-SystemVerilog/blob/main/Screenshots/TCL_Console_3.png?raw=true)



## **Conclusion**

This project verifies the functionality of a FIFO buffer using SystemVerilog, employing mailbox communication and scoreboarding for robust validation. The testbench automates result checking, ensuring correctness in write, read, and reset operations. Constrained-random stimulus and transaction-based modeling enhance test coverage, while the scoreboard ensures accurate output comparison. This project demonstrates industry-standard verification techniques and can be extended with assertions, functional coverage, and corner-case testing for improved reliability.


