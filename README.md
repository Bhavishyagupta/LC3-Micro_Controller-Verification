LC-3 Microcontroller Verification (SystemVerilog & UVM)
Overview

This project focuses on the verification of an LC-3–style microcontroller using a SystemVerilog UVM-based verification environment. The goal is to ensure functional correctness, control behavior validation, and coverage-driven confidence for a CPU-style design.

The environment is structured to support directed testing, constrained-random instruction streams, and scalable verification components, similar to industry-grade CPU and SoC verification flows.

Project Objectives

Verify correct execution of LC-3 instructions

Validate control logic, datapath behavior, and state updates

Build a reusable and scalable UVM verification environment

Achieve high functional coverage through constrained-random testing

Verification Environment

The verification framework is built using UVM and follows a modular architecture:

Transaction-level modeling of instruction behavior

Monitors and analysis ports for observing DUT activity

Predictor modeling expected architectural behavior

Scoreboard for cycle-accurate functional comparison

Support for multiple test types and random seeds

What is Verified

Instruction decode correctness

ALU operations (ADD, AND, NOT)

Load and store operations

Control-flow behavior (branches and jumps)

Condition codes (NZP) updates

Architectural state consistency across instructions

Test Strategy

Directed tests for initial bring-up and sanity checking

Constrained-random instruction streams to explore corner cases

Coverage-driven refinement to improve stimulus quality

The testbench allows flexible control over instruction mix, operand values, and execution scenarios.

Coverage

Opcode-level functional coverage

Control and condition-code coverage

Coverage closure supported via randomized stimulus

Repository Structure
├── rtl/           # LC-3 microcontroller RTL
├── tb/            # UVM testbench top
├── env/           # Environment, scoreboard, predictor
├── sequences/     # Directed and random sequences
├── tests/         # UVM tests
├── scripts/       # Simulation scripts / Makefile
└── docs/          # Design and verification notes

How to Run (Conceptual)

Compile RTL and verification environment

Select a test using UVM_TESTNAME

Run simulation and analyze logs and coverage

Example:

+UVM_TESTNAME=lc3_random_test
+UVM_VERBOSITY=UVM_MEDIUM

Skills Demonstrated

SystemVerilog & UVM

CPU / microcontroller verification concepts

Scoreboard and reference-model based checking

Constrained-random testing and coverage closure

Debug and failure triage
