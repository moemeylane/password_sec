# password_sec
# LAB 7 & 8
# file hashes.py
This script generates MD5, SHA1, and SHA256 hashes for a given password. 
To run:


Copy

`python generate_hashes.py`
You’ll be prompted to enter a password, and the script will print:

MD5 hash

SHA1 hash

SHA256 hash

# Example:
Input: 
Copy
Enter password to hash: `password`

Output:

Original password: password  
MD5: 5f4dcc3b5aa765d61d8327deb882cf99  
SHA1: 5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8  
SHA256: 5e884898da28047151d0e56f8dc6292773603d0d6aabbdd62a11ef721d1542d8
# Cracking with John the Ripper
# File: hashes.txt
Paste the MD5 hash into hashes.txt in this format:


Copy
`$dynamic_0$5f4dcc3b5aa765d61d8327deb882cf99`
📦 Crack with:
Copy
`john --format=Raw-MD5 --wordlist=rockyou.txt hashes.txt`
To view the result after cracking:

Copy

`john --show hashes.txt`
💡 Ensure John the Ripper is installed:
IF NOT ;

Copy

`sudo apt install john` for linux environment
for windows environment : Download Precompiled Binaries: You can download the Windows binaries from the official `John the Ripper website `
# Lab 8: Zero-Knowledge Proof (ZKP) Implementation
# File: zkp_demo.py
This script demonstrates a simple Zero-Knowledge Proof using modular arithmetic. It simulates how a prover can convince a verifier that they know a secret without revealing the secret itself.

✅ Usage:

Copy
`python zkp_demo.py`
# Key Concepts:
secret_number: A value known only to the prover

base and modulus: Public parameters

public_value: Derived from the secret, shared publicly

commitment: Sent by the prover

challenge: Random bit (0 or 1) from the verifier

response: Prover's reply based on the challenge

check: Verifier checks if the prover was honest

The script prints each step clearly to show how Zero-Knowledge Proof works.
