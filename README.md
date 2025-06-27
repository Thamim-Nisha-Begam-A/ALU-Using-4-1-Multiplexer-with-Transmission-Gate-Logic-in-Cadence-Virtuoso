# ALU-Using-4-1-Multiplexer-with-Transmission-Gate-Logic-in-Cadence-Virtuoso
This project demonstrates the implementation of a 1-bit ALU using 4×1 mux, entirely constructed from Transmission Gate Logic (TGL) within the Cadence Virtuoso environment. The design emphasizes minimal transistor-level logic and optimized switching behavior to perform basic logic operations—AND, OR, NAND, and NOR—selected via control lines.
Design Overview:
The 4×1 MUX is architected using three 2×1 multiplexers, each built from transmission gates to ensure high-speed, bidirectional signal flow with low power dissipation.

All core logic gates (AND, OR, NAND, NOR) are constructed using transmission gate-based circuits instead of standard CMOS logic, providing a unified, consistent logic family throughout the ALU.

The multiplexer acts as a functional selector. Depending on the 2-bit select lines, the MUX routes one of the four logic gate outputs as the final ALU output.
Functional Mapping:
Select Lines (S1, S0)	Operation	Output Logic
00	AND	A • B
01	OR	A + B
10	NAND	¬(A • B)
11	NOR	¬(A + B)
Implementation Notes:
Each 2×1 multiplexer uses 2 transmission gates and 1 inverter for control inversion.

Logic gates are designed using pass-transistor logic principles, prioritizing compactness and energy efficiency.

Simulations in Cadence Virtuoso confirm correct operation for all input combinations and selection cases.

Scalability:
Although currently implemented for a 1-bit operation, this structure can be extended to build multi-bit ALUs by replicating the circuit for each bit and synchronizing their select lines.
