# Simple Substitution Cipher Encryption and Decryption

This project implements a simple substitution cipher using Python. The program encrypts and decrypts messages based on a shuffled key derived from all ASCII printable characters. The characters include letters, digits, punctuation, and whitespace. The code is a basic example of how substitution ciphers work and provides a way to encrypt and decrypt text using a random key.

## Table of Contents
- [Overview](#overview)
- [How It Works](#how-it-works)
- [Setup and Usage](#setup-and-usage)
- [Example](#example)
- [Notes](#notes)

## Overview
A substitution cipher replaces each character in the plaintext message with a corresponding character from a shuffled set. The same shuffled set (key) is used to decrypt the cipher text back to the original message. This simple project demonstrates the concept by using all printable ASCII characters.

## How It Works
1. **Key Generation**: 
   - The code creates a list of all printable characters (`chars`) which includes:
     - Letters (uppercase and lowercase)
     - Digits (0-9)
     - Punctuation (`!@#$%^&*()`, etc.)
     - Whitespace (` `)
   - A copy of this list (`key`) is shuffled randomly to form a substitution key.

2. **Encryption**:
   - The user provides a plaintext message.
   - Each character in the message is replaced by its corresponding character in the shuffled key.
   - The result is an encrypted message.

3. **Decryption**:
   - The user provides the encrypted message.
   - Each character in the cipher text is replaced by the corresponding character from the original list (`chars`), based on the shuffled key (`key`).
   - The result is the original plaintext message.

## Setup and Usage

### Prerequisites
- Python 3.x installed on your system.

### Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/substitution-cipher.git
   cd substitution-cipher
   ```

2. Run the program:
   ```bash
   python substitution_cipher.py
   ```

3. Follow the prompts to enter a message for encryption and decryption.

## Example

Here's an example interaction with the program:

```
msg to encrypt: Hello, World!
encrypted msg: &Aq2o?P>CtB4
msg to encrypt: &Aq2o?P>CtB4
original msg: Hello, World!
```

## Notes
- The same `key` used to encrypt must be retained to decrypt the message. If the `key` changes, the decryption will not produce the correct output.
- The cipher implemented here is not secure for practical purposes. It's a simple demonstration and lacks the complexity of modern encryption algorithms.
