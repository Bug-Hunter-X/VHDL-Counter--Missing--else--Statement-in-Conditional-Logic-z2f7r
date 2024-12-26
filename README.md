# VHDL Counter Bug

This repository demonstrates a common error in VHDL code: a missing 'else' statement in conditional logic within a counter process.  The `buggy_counter.vhdl` file contains the erroneous code, while `fixed_counter.vhdl` provides the corrected version.

The bug results in unexpected behavior when the counter reaches its maximum value (15 in this case). The improved version ensures proper handling of all possible scenarios.

## How to Reproduce the Bug
1. Simulate `buggy_counter.vhdl` using your preferred VHDL simulator.
2. Observe the counter's behavior when it reaches its maximum value (15).
3. Compare this behavior to the expected behavior (wrapping around to 0).

## Solution
The missing 'else' statement causes the counter to potentially remain at 15, rather than resetting to 0. The fix simply adds a default case to reset the counter when it reaches 15. 