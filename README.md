# Task 6: Introduction to Cryptography

## 📌 Overview
This task demonstrates the fundamental concepts of cryptography including symmetric encryption, asymmetric encryption, hashing, and digital signatures. Practical implementation is performed using OpenSSL to understand real-world secure communication mechanisms.

---

## 🎯 Objectives
- Understand the basics of cryptography
- Perform symmetric encryption using AES
- Generate asymmetric RSA key pairs
- Verify data integrity using hashing
- Create and verify digital signatures
- Learn real-world applications of cryptography

---

## 🛠 Tools Used
- OpenSSL
- Terminal / Command Prompt
- Operating System: Linux / Windows

---

## 🔐 Symmetric Encryption (AES)

### Description
AES (Advanced Encryption Standard) is a symmetric encryption algorithm that uses a single shared key for both encryption and decryption.

### Commands Used
```bash

echo "This is a secret message" > secret.txt
openssl enc -aes-256-cbc -salt -in secret.txt -out secret.enc

openssl enc -aes-256-cbc -d -in secret.enc -out decrypted.txt

🔑 Asymmetric Encryption (RSA)
Description
RSA is an asymmetric encryption algorithm that uses a public key and a private key.

Commands Used
openssl genrsa -out private.pem 2048
openssl rsa -in private.pem -pubout -out public.pem
🧮 Hashing & Integrity (SHA-256)
Description

Hashing ensures data integrity. Any change in the file results in a different hash value.

Commands Used
openssl dgst -sha256 secret.txt
echo "changed" >> secret.txt
openssl dgst -sha256 secret.txt

Result

Hash value changes after file modification, confirming integrity verification.
✍ Digital Signature
Description

Digital signatures ensure authenticity, integrity, and non-repudiation of data.

Commands Used
openssl dgst -sha256 -sign private.pem -out sign.bin secret.txt
openssl dgst -sha256 -verify public.pem -signature sign.bin secret.txt

Result

Signature verification returns Verified OK.

📊 Algorithm Comparison
Algorithm	Type	Purpose
AES	Symmetric	Fast data encryption
RSA	Asymmetric	Secure key exchange
SHA-256	Hash	Data integrity


---

### ✅ What You Can Do Now
- Push this `README.md` + screenshots to **GitHub**
- Submit along with **PDF report**
- Use it for **college practical / cybersecurity task**

If you want, I can:
- 🧾 Add **student name, enrollment no., subject**
- 📄 Convert README → **PDF**
- 🧩 Match **GTU / university format**

Just tell me 👌
