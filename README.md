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
def xor_crypt(input_text, key):
    output = []
    key_length = len(key)

    for i in range(len(input_text)):
        xor_char = chr(ord(input_text[i]) ^ ord(key[i % key_length]))
        output.append(xor_char)

    return ''.join(output)


# Main program
msg = input("Enter message: ")
key = input("Enter key: ")

# Encrypt
enc = xor_crypt(msg, key)

print("Encrypted:", end=" ")
for ch in enc:
    print(f"{ord(ch):02X}", end=" ")
print()

# Decrypt
dec = xor_crypt(enc, key)
print("Decrypted:", dec)
```




## Output:

<img width="819" height="268" alt="image" src="https://github.com/user-attachments/assets/2f5454a9-0909-4ef5-b919-4c9dacc43190" />

## Result:
  The program is executed successfully

