# Unintentional Latch in VHDL

This repository demonstrates a common, subtle bug in VHDL code: an unintentional latch created by incomplete signal assignments within a process.  The provided `bug.vhdl` file showcases this issue. The solution, `bugSolution.vhdl`, corrects the problem.

**Problem:** The original code lacks a complete assignment for the `internal_data` signal in all cases of the clock cycle.  This results in an implicit latch being created by the synthesizer, leading to unpredictable behavior and potentially unwanted functionality.

**Solution:**  The corrected code explicitly assigns values to all signals, regardless of the clock edge, thereby removing the latch. 

This example highlights the importance of meticulously handling signal assignments in VHDL processes to prevent such subtle but problematic errors.