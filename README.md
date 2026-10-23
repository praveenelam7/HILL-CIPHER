# HILL CIPHER
HILL CIPHER
EX. NO: 3 AIM:
 

IMPLEMENTATION OF HILL CIPHER
 
## To write a C program to implement the hill cipher substitution techniques.

## DESCRIPTION:

Each letter is represented by a number modulo 26. Often the simple scheme A = 0, B
= 1... Z = 25, is used, but this is not an essential feature of the cipher. To encrypt a message, each block of n letters is  multiplied by an invertible n × n matrix, against modulus 26. To
decrypt the message, each block is multiplied by the inverse of the m trix used for
 
encryption. The matrix used
 
for encryption is the cipher key, and it sho
 
ld be chosen
 
randomly from the set of invertible n × n matrices (modulo 26).


## ALGORITHM:

STEP-1: Read the plain text and key from the user. STEP-2: Split the plain text into groups of length three. STEP-3: Arrange the keyword in a 3*3 matrix.
STEP-4: Multiply the two matrices to obtain the cipher text of length three.
STEP-5: Combine all these groups to get the complete cipher text.

## PROGRAM 

```
#include <stdio.h>
#include <ctype.h>

int main()
{
    char text[100];
    int a, b, x, y, i;
    int k[2][2] = {{3, 3}, {2, 5}};

    printf("Enter text: ");
    scanf("%99s", text);

    for (i = 0; text[i] != '\0'; i += 2)
    {
        a = toupper(text[i]) - 'A';
        b = text[i + 1] ? toupper(text[i + 1]) - 'A' : 23;

        x = (3*a + 3*b) % 26;
        y = (2*a + 5*b) % 26;

        printf("%c%c", x + 'A', y + 'A');
    }

    return 0;
}
```
## OUTPUT
<img width="1485" height="757" alt="image" src="https://github.com/user-attachments/assets/ff8b1dee-901b-47ec-884b-90e42a64cf3d" />


## RESULT

Thus, the Hill Cipher encryption program was executed successfully, and the given plaintext was encrypted into ciphertext using a 2×2 key matrix.
