# Parity-Generator

Overview

This project demonstrates the design and verification of a 4-bit Parity Generator. The module calculates both even parity and odd parity for a given 4-bit input.

Features:

Even Parity: The XOR of all input bits, representing an even parity bit.
Odd Parity: The complement of the even parity bit, representing an odd parity bit.

RTL Code
Module: parity_generator

Inputs:

data_in [3:0]: A 4-bit input vector.

Outputs:

even_parity: A single bit representing the even parity.
odd_parity: A single bit representing the odd parity.

Functionality:

The module computes the even parity using the XOR operation over all bits in data_in.
The odd parity is derived as the complement of the even parity.

Testbench

Module: tb_parity_generator

Purpose:

The testbench is designed to verify the functionality of the parity generator module.

Components:

Inputs:

data_in: A 4-bit vector driven with various test patterns.

Outputs:

even_parity and odd_parity: Outputs from the parity_generator module.

Device Under Test (DUT):

The parity_generator module is instantiated as uut.

Verification:

initial block drives various input patterns into the DUT.
$monitor prints the results to verify parity generation.

Test Patterns:

4'b0000

4'b0001

4'b0011

4'b0111

4'b1111

4'b1010

4'b0101

The results are printed with simulation time, input, even parity, and odd parity.

 Output

The following results should be displayed during simulation:

Time=0 | Data_in=0000 | Even_Parity=0 | Odd_Parity=1

Time=10 | Data_in=0001 | Even_Parity=1 | Odd_Parity=0

Time=20 | Data_in=0011 | Even_Parity=0 | Odd_Parity=1

Time=30 | Data_in=0111 | Even_Parity=1 | Odd_Parity=0

Time=40 | Data_in=1111 | Even_Parity=0 | Odd_Parity=1

Time=50 | Data_in=1010 | Even_Parity=0 | Odd_Parity=1

Time=60 | Data_in=0101 | Even_Parity=0 | Odd_Parity=1
