LC-3 Microcontroller Verification

This repository contains a SystemVerilog UVM-based verification environment for an LC-3 style microcontroller. The project focuses on verifying instruction execution, control behavior, and architectural state correctness using directed and constrained-random testing.

Overview

The verification environment is built using UVM and is structured to be modular, scalable, and easy to debug. It follows verification practices commonly used for CPU and microcontroller designs.

The testbench supports both directed tests for bring-up and constrained-random instruction streams for functional coverage.

Project Goals

Verify correct execution of LC-3 instructions
Validate ALU, control, and datapath behavior
Build a reusable UVM verification framework
Achieve functional coverage using randomized testing

Verification Methodology

UVM-based modular testbench
Transaction-level modeling
Predictor and scoreboard based checking
Directed and constrained-random tests

Verified Functionality

Instruction decode
ALU operations such as ADD, AND, and NOT
Load and store instructions
Branch and jump behavior
Condition code NZP updates
Architectural state consistency

Test Strategy

Directed sanity tests for initial validation
Random instruction sequences for coverage
Coverage-driven refinement of stimulus

Coverage

Opcode-level coverage
Control and condition-code coverage

Repository Structure

rtl LC-3 microcontroller RTL
tb UVM testbench top
env Environment, predictor, scoreboard
sequences Directed and random sequences
tests UVM tests
scripts Simulation scripts
docs Design and verification notes

Running Simulations

Select a test using the UVM_TESTNAME argument when running the simulator.

Example run options:

+UVM_TESTNAME=lc3_random_test
+UVM_VERBOSITY=UVM_MEDIUM

Skills Demonstrated

SystemVerilog and UVM
CPU and microcontroller verification
Scoreboard and reference model checking
Constrained-random testing
Functional coverage
