
# EX.8 Implement the AES Encryption and decryption

# AIM:
Implementation of the AES Encryption and decryption

# ALGORITHM:
1.	Install Necessary Libraries
2.	Generate a random 128-bit key (which is 16 bytes).
3.	AES requires input data to be a multiple of 16 bytes. Here's a simple padding function:
4.	Encrypt your plaintext using AES in ECB (Electronic Codebook) mode:
5.	Decrypt the ciphertext back to plaintext:

# PROGRAM:

```C

#include <stdio.h>
#include <string.h>
void simpleAESEncrypt(char *plaintext, char *key, char *ciphertext)
{
int i;
for (i = 0; i < strlen(plaintext); i++)
{
ciphertext[i] = plaintext[i] ^ key[i % strlen(key)];
}
ciphertext[i] =
'\0';
}
void simpleAESDecrypt(char *ciphertext, char *key, char *decryptedText)
{
int i;
for (i = 0; i < strlen(ciphertext); i++)
{
decryptedText[i] = ciphertext[i] ^ key[i % strlen(key)];
}
decryptedText[i] =
'\0';
}
void printASCII(char *ciphertext)
{
printf("Encrypted Message (ASCII values): ");
for (int i = 0; i < strlen(ciphertext); i++)
{
printf("%d "
, (unsigned char)ciphertext[i]);
}
printf("\n");
}
int main()
{
char plaintext[100], key[100], ciphertext[100], decryptedText[100];
printf("Enter the plaintext: ");
scanf("%s"
, plaintext);
printf("Enter the key: ");
scanf("%s"
, key);
simpleAESEncrypt(plaintext, key, ciphertext);
printASCII(ciphertext);
simpleAESDecrypt(ciphertext, key, decryptedText);
printf("Decrypted Message: %s\n"
, decryptedText);
return 0;
}

```

# OUTPUT:
![Screenshot 2024-11-14 135940](https://github.com/user-attachments/assets/0d38999f-5e2a-4b7d-855a-f2ed636f7131)



# RESULT:
	Hence, for the given input text and key for Implementing the AES Encryption and decryption is successfully simulated.
