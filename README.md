## Hybrid Quantum-Classical Cryptographic Framework for Secure Data Communication

A robust security framework that seamlessly integrates the information-theoretic security of Quantum Key Distribution (QKD) with the efficiency of classical AES-256 encryption to protect data against future quantum computing threats.

## About
The rapid evolution of quantum computing poses a significant existential threat to traditional cryptographic systems like RSA and Elliptic Curve Cryptography (ECC), which rely on mathematical assumptions vulnerable to quantum algorithms such as Shor’s. This project, **Hybrid Quantum-Classical Cryptographic Framework**, is designed to bridge the gap between current security infrastructure and the post-quantum era.

The framework employs a layered security approach:
1.  [cite_start]**Quantum Layer**: Utilizes a simulated **BB84 protocol** to generate shared secret keys, ensuring that any eavesdropping attempts are physically detectable[cite: 34].
2.  [cite_start]**Authentication Layer**: Integrates **Post-Quantum Cryptography (PQC)** algorithms (specifically lattice-based methods like CRYSTALS-Dilithium) to prevent man-in-the-middle attacks[cite: 35].
3.  [cite_start]**Classical Layer**: Uses the generated hybrid keys within **AES-256 (Galois/Counter Mode)** for high-speed, authenticated data encryption[cite: 36].

This system provides a practical, scalable migration path for organizations to enhance their security posture without a complete overhaul of existing TCP/IP network infrastructures.

## Features
- [cite_start]**Quantum Key Distribution (QKD):** Implements a simulation of the BB84 protocol using Qiskit to generate high-entropy keys with eavesdropping detection[cite: 222, 225].
- [cite_start]**Hybrid Key Derivation:** Combines quantum-generated keys with classical/post-quantum salts using SHA-256 to derive secure session keys, ensuring resilience even if one source is compromised[cite: 190, 250].
- [cite_start]**Post-Quantum Authentication:** Utilizes lattice-based digital signatures to authenticate users and session handshakes, resisting quantum adversaries[cite: 194].
- [cite_start]**Authenticated Encryption:** Deploys AES-256 in GCM mode to provide both data confidentiality and integrity verification[cite: 199, 201].
- [cite_start]**Forward Secrecy:** Enforces automated key rotation and secure memory erasure of old keys to prevent future decryption of past sessions[cite: 206].
- [cite_start]**Tamper Detection:** Automatically detects and aborts sessions if high error rates (indicating eavesdropping) or integrity check failures are detected[cite: 385].

## Requirements
* [cite_start]**Operating System:** Windows, Linux, or macOS[cite: 150].
* [cite_start]**Processor:** Intel i5 / Ryzen 5 or higher[cite: 145].
* [cite_start]**RAM:** 8–16 GB (Recommended for quantum simulation operations)[cite: 146].
* [cite_start]**Language:** Python 3.x[cite: 151].
* [cite_start]**Cryptography Libraries:** `PyCryptodome` for AES-256 (GCM), SHA-256, and HMAC operations[cite: 152].
* [cite_start]**Quantum Simulation:** `Qiskit` framework for simulating qubits and the BB84 protocol[cite: 152].
* [cite_start]**Networking:** Standard Python `socket` library for TCP/IP communication[cite: 152].
* [cite_start]**IDE:** VS Code (Recommended)[cite: 153].

## System Architecture
The architecture consists of five robust layers: User, Application, Security, Storage, and Communication. The core logic resides in the Security Layer, where the Key Management module orchestrates the Quantum Module (BB84), Post-Quantum Auth Module, and the Classical Crypto Engine.

![System Architecture Diagram](https://github.com/<<yourusername>>/Hybrid-Quantum-Crypto-Framework/assets/path-to-your-architecture-image)
[cite_start]*(Note: Refer to Figure 5.1 in the project documentation for the visual diagram [cite: 171])*

## Output

#### Output 1 - System Initialization & QKD
The console log below demonstrates the BB84 protocol simulation. It shows the generation of random qubits, basis selection by Alice and Bob, and the sifting process where mismatched bases are discarded to form the raw quantum key.

![System Initialization Output](https://github.com/<<yourusername>>/Hybrid-Quantum-Crypto-Framework/assets/path-to-your-init-image)
[cite_start]*[cite: 367]*

#### Output 2 - Encryption & Secure Transmission
This output details the classical encryption phase. The system takes the plaintext (e.g., "Confidential Medical Record"), derives a hybrid session key, and generates the Ciphertext and Authentication Tag using AES-GCM before transmission.

![Encryption Process Output](https://github.com/<<yourusername>>/Hybrid-Quantum-Crypto-Framework/assets/path-to-your-encryption-image)
[cite_start]*[cite: 372]*

#### Output 3 - Decryption & Integrity Verification
At the receiver's end, the log confirms the receipt of the payload. It explicitly states **"Integrity Verified"** (proving no tampering occurred) before decrypting the ciphertext back to the original plaintext.

![Decryption Output](https://github.com/<<yourusername>>/Hybrid-Quantum-Crypto-Framework/assets/path-to-your-decryption-image)
[cite_start]*[cite: 378]*

## Results and Impact
This project successfully demonstrates that quantum principles can be simulated and integrated into standard network architectures. 
- [cite_start]**Security:** Validated against both black-box and white-box testing, resisting replay attacks, tampering, and unauthorized access[cite: 288].
- [cite_start]**Performance:** Achieved high-speed encryption for bulk data using AES-256 while maintaining quantum-safe key exchange[cite: 284].
- [cite_start]**Impact:** Establishes a viable blueprint for "Quantum-Safe" communications, allowing critical infrastructure to prepare for the post-quantum era without requiring immediate, expensive hardware upgrades[cite: 290].

## Articles published / References
1. [cite_start]Raj, A., and Balachandran, V., “A Hybrid Encryption Framework Combining Classical, Post-Quantum, and QKD Methods,” *arXiv preprint arXiv:2509.10551*, 2025[cite: 388].
2. [cite_start]Sanz, A., et al., “Extending Quantum-Safe Communications to Real-World Networks: An Adaptive Security Framework,” *arXiv preprint arXiv:2511.22416*, 2025[cite: 389].
3. [cite_start]Mozo, H. E., “Quantum-Classical Hybrid Encryption Framework Based on Simulated BB84 and AES-256,” *arXiv preprint arXiv:2511.02836*, 2025[cite: 390].
4. Shafique, A., et al., “A Hybrid Encryption Framework Leveraging Quantum and Classical Cryptography,” *Scientific Reports*, vol. [cite_start]14, 2024[cite: 391].
5. [cite_start]Angamuthu, G., and Marikkannan, M., “Hybrid Quantum-Resistant Key Exchange Protocol for Secure Network Communication,” *IJCSE*, 2025[cite: 393].
