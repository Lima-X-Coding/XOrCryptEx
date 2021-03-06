# XOrCryptEx (C/C++)
XOrCryptEx is a lightweight Xorcrypt algorithm that uses chaining and bitwise array rotation.\
It was designed to be extremly light on resources and has little to no overhead,
as well as being very fast.\
It is also nativly compatible with 8-, 16-, 32- and 64-Bit CPU's

## How it works
-> Xor Plaintext-Block with Key-Block (return Ciphertext)\
-> Xor Key-Block with Paintext-Block (using temporary copy of Plaintext-Block)\
-> Bitwise array rotate Key\
-> repeate until done

![SCHEM](https://github.com/Lima-X-Coding/XOrCrypt/blob/master/XOrCrypt.png)
## Comment
I don't really know how good the protection/encryption exactly is (in statistical means),
but it should be pretty strong for an Xorcrypt algorithm and for the amount of code it requires.\
Because the Key gets xored with the Plaintext,
it constantly changes meaning that every Big Block of the Plaintext gets it's on pseudoKey.\
The rotation just add's an additional layer of protection by making it harder to reverse engineer
the Key using part of the Plaintext (if it is known or can be predicted),
this is achived by introducing an "offset" in the key.

If you want to use this you just need to include `XOrCrypt.h` and `XOrCrypt.c` in your project.\
(XOrCryptEx.cpp was just for testing and debugging purposes, it might help tho to understand how to use it.)
