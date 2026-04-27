# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
```
#include <stdio.h>
#include <string.h>

void xor_fun(char *a, char *k) {
    int i;
    for(i=0;i<strlen(a);i++)
        a[i] = a[i] ^ k[i % strlen(k)];
}

int main() {
    char url[] = "Bhoopesh";
    char key[] = "megu";

    printf("Original: %s\n", url);

    xor_fun(url, key);

    printf("Encrypted: ");
    for(int i=0;i<strlen(url);i++)
        printf("%02X ", (unsigned char)url[i]);

    printf("\n");

    xor_fun(url, key);
    printf("Decrypted: %s\n", url);

    return 0;
}
```
# OUTPUT:
<img width="1208" height="483" alt="image" src="https://github.com/user-attachments/assets/f8a8a878-97bc-43e4-b6da-ac44229002a9" />


# RESULT:

Hence the experiment has been executed successfully
