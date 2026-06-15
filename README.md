# EX-NO-7-Implement-DES-Encryption

## Aim:

To use the Data Encryption Standard (DES) algorithm for a practical application, such as securing sensitive data transmission in financial transactions.

## ALGORITHM:

1. DES is based on a symmetric key encryption technique that encrypts data in 64-bit blocks.
2. DES uses a Feistel network structure with 16 rounds of processing for encryption.
3. DES has a 64-bit key, but only 56 bits are used for encryption (the remaining 8 bits are for parity).
4. DES applies initial and final permutations along with 16 rounds of substitution and permutation transformations to produce ciphertext.

## Program:
```
def xor_encrypt(text, key):
    result = ""

    for i in range(len(text)):
        ch = chr(ord(text[i]) ^ ord(key[i % len(key)]))
        result += ch

    return result

message = input("Enter message: ")
key = input("Enter key: ")

encrypted = xor_encrypt(message, key)

print("Encrypted:", end=" ")
for ch in encrypted:
    print(format(ord(ch), "02X"), end=" ")

decrypted = xor_encrypt(encrypted, key)

print("\nDecrypted:", decrypted)

```



## Output:
<img width="226" height="68" alt="image" src="https://github.com/user-attachments/assets/2095841d-8375-43bf-bf4d-5e88f13c996e" />


## Result:
  The program is executed successfully

