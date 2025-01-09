# VHDL Counter Overflow Bug

This repository demonstrates a common bug in VHDL code: an integer counter that overflows without any error handling.  The `buggy_counter.vhd` file contains the erroneous code. The `fixed_counter.vhd` file shows the corrected code.

## Bug Description

The counter increments indefinitely, wrapping around from 15 to 0. This behavior might be unintentional.  The bug is not flagged by most VHDL simulators but can lead to unexpected behaviour in the synthesized hardware.

## Solution

The `fixed_counter.vhd` file demonstrates a solution which prevents the counter from exceeding the maximum value by adding a check before incrementing.