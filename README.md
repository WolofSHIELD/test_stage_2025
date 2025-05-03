✅ Technical Test – TFHE Implementation (Rust or C)
🎯 Objective
Implement a minimal homomorphic encryption system using TFHE, capable of:

🔐 Encrypting two bits (a = 1, b = 0)

⚙️ Evaluating a logical operation (XOR or AND) homomorphically

🔓 Decrypting and displaying the result

🛠️ Allowed Languages
Rust with tfhe-rs (Zama)

C/C++ with tfhe (original library)

🗂️ Project Structure
css
Copier
Modifier
TFHE_Test/
├── README.md
├── src/
│   ├── main.rs / main.c
│   └── (additional source files if needed)
├── Cargo.toml / Makefile
└── output.txt         # Expected output sample
📝 Instructions
🔧 Required Steps
✅ Initialize the TFHE key system (secret + cloud keys)

✅ Encrypt two input bits (a = 1, b = 0)

✅ Perform a homomorphic XOR or AND

✅ Decrypt the result and print it

✅ Measure execution time for:

Encryption

Evaluation

Decryption

📌 Requirements
The code must be well-documented

The project must compile and run without errors

README.md must clearly state:

Setup instructions and dependencies

Build and execution commands

Example of expected output

🔧 Suggested Libraries
Rust: tfhe-rs

C/C++: tfhe

📤 Submission
Submit the project as a .zip archive or via a private GitHub repository

Recommended deadline: within 72 hours of receiving the test
