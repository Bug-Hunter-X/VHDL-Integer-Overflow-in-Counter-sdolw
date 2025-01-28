# VHDL Integer Overflow Bug

This repository demonstrates a potential integer overflow bug in a simple VHDL counter. The `buggy_counter.vhdl` file contains the buggy code, while `fixed_counter.vhdl` provides a corrected version.

## Bug Description
The original counter uses an `integer` type, which is unbounded in VHDL.  When the counter reaches its maximum value (15 in this case), incrementing it leads to unpredictable behavior. The simulation might wrap around to a negative value or show a different unexpected behavior. 

## Solution
The solution involves using an unsigned type with a defined range, ensuring that overflow is handled correctly, preventing unexpected values. The corrected code is presented in `fixed_counter.vhdl`, which uses `unsigned` type preventing the overflow and ensures a predictable behavior.
