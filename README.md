# Rust Unsafety Bug
This repository demonstrates a potential issue when working with unsafe Rust code and mutable references.  The `bug.rs` file shows code that directly manipulates memory using raw pointers, leading to potential undefined behavior if not managed correctly. The `bugSolution.rs` file provides a safer alternative using Rust's safe abstractions.

## Problem
The original `bug.rs` code modifies a vector using a raw pointer.  While this may appear functional, it bypasses Rust's memory safety guarantees.  This can cause unexpected crashes, data corruption, or other subtle issues, making it difficult to debug. The modification of v via a raw pointer will not update the length of the vector, potentially leading to memory safety issues.

## Solution
The `bugSolution.rs` demonstrates a safe approach using Rust's standard library functions. Instead of directly manipulating memory, it uses vector's indexing capabilities and built-in functions, preserving memory safety.

## How to Run
1. Clone this repository.
2. Navigate to the repository's directory.
3. Compile and run each file using `rustc bug.rs && ./bug` and `rustc bugSolution.rs && ./bugSolution`.