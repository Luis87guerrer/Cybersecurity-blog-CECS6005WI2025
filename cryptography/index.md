---
layout: page
title: Cryptography
permalink: /cryptography/
---

# Cryptography: how we make data safe in a world that can’t be trusted

Every time you log into a website, send a message, tap-to-pay, or store files in the cloud, you’re depending on cryptography.

Cryptography is the collection of methods used to protect information by transforming it so that unauthorized people cannot read it—and so that tampering is detectable. Modern cryptography supports not only secrecy, but also trust: *who sent this, did it change, can we prove it?*

## The basic idea (plaintext → ciphertext → plaintext)
- **Plaintext:** normal readable data
- **Encryption:** transforms plaintext into **ciphertext**
- **Ciphertext:** unreadable output
- **Decryption:** converts ciphertext back to plaintext (for authorized users)

The magic isn’t really magic—it’s math + keys.

## What cryptography provides (the security goals)
Cryptography is usually tied to four major outcomes:

### Confidentiality
Only authorized users can read the data (even if someone intercepts it).

### Integrity
If someone changes the data, the change can be detected.

### Authentication
You can verify identity or verify the source of a message.

### Non-repudiation
A sender can’t easily deny they performed an action (commonly supported by digital signatures).

## The three “big building blocks”
Most real security systems combine these tools:

### 1) Symmetric encryption (one shared key)
Symmetric crypto uses the same key to encrypt and decrypt.
- **Strength:** very fast, great for large files or large data streams.
- **Weakness:** key sharing is hard—how do you safely give the key to the other party?

This is why websites don’t use only symmetric encryption. They combine it with asymmetric crypto for key exchange.

### 2) Asymmetric encryption (public key / private key)
Asymmetric crypto uses a key pair:
- **Public key:** share it openly
- **Private key:** keep it secret

If I encrypt with your public key, only your private key can decrypt it. This enables:
- secure key exchange
- digital signatures
- identity verification (when combined with certificates)

### 3) Hash functions (one-way fingerprints)
A **hash** turns data into a fixed-length “digest.”
- small change in input → huge change in digest
- typically one-way (you don’t decrypt a hash)

Hashes are used for integrity checks, digital signatures, and password storage (when used with salts and slow hashing methods).

## Key management: the hidden “real” problem
Strong algorithms can still fail if keys are handled poorly. Key management includes:
- generation (strong randomness)
- storage (hardware security modules or secure vaults)
- rotation (changing keys on schedule or after compromise)
- access control (who can use keys)
- revocation (what happens when a key is exposed)

In practice, “crypto failures” are often “key failures.”

## Where cryptography shows up in real life
### Secure web browsing (TLS/HTTPS)
When your browser shows HTTPS, cryptography is happening:
- the site proves identity (certificates)
- you establish encrypted communication (keys)
- data is protected in transit

### Disk and file encryption
Cryptography protects laptops, phones, and cloud storage so stolen devices don’t automatically leak data.

### Authentication systems
Cryptography supports:
- password hashing (so databases don’t store plaintext passwords)
- tokens and sessions
- secure MFA mechanisms

### Digital signatures
Used to prove who signed code, documents, or transactions—and to detect tampering.

## Common mistakes beginners make
- Confusing **encoding** with encryption (encoding is for format; encryption is for security).
- Thinking encryption alone is enough (but keys, access, and backups still matter).
- Ignoring integrity (confidentiality without integrity can still be dangerous).
- Reusing keys or weak passwords as “keys” (key strength matters).

## References
- ISO — What is cryptography?: https://www.iso.org/information-security/what-is-cryptography  
- IBM — What is cryptography?: https://www.ibm.com/think/topics/cryptography  
- GeeksforGeeks — Cryptography and its types: https://www.geeksforgeeks.org/computer-networks/cryptography-and-its-types/  

