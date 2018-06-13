# RSA-Encryption
A simple implementation of RSA encryption using python 3.5

Introduction to RSA Encryption:

This is how it works:-
Choose two distinct prime numbers p and q.
For security purposes, the integers p and q should be chosen at random, and should be similar in magnitude but differ in length by a few digits to make factoring harder. Prime integers can be efficiently found using a primality test.
Compute n = pq.
n is used as the modulus for both the public and private keys. Its length, usually expressed in bits, is the key length.
Compute λ(n) = lcm(λ(p), λ(q)) = lcm(p − 1, q − 1), where λ is Carmichael's totient function. This value is kept private.
Choose an integer e such that 1 < e < λ(n) and gcd(e, λ(n)) = 1; i.e., e and λ(n) are coprime.
Determine d as d ≡ e−1 (mod λ(n)); i.e., d is the modular multiplicative inverse of e (modulo λ(n)).
This is more clearly stated as: solve for d given d⋅e ≡ 1 (mod λ(n)).
e having a short bit-length and small Hamming weight results in more efficient encryption – most commonly e = 216 + 1 = 65,537. However, much smaller values of e (such as 3) have been shown to be less secure in some settings.
e is released as the public key exponent.
d is kept as the private key exponent.

I recommend reading the wiki page: https://en.wikipedia.org/wiki/RSA_(cryptosystem)


Initially I have used 2 to 5 digit numbers for random prime generation. If you wanna make it more secure, increase the number of digits by  changing this: (length=5) to (length=x). But time complexity will increase directly proportional to number of digits.

Few may wonder why I have not used functions in places. But there is a reason behind it.

The program randomly generates two prime numbers, calculates phi(n), asks you to choose one from list of provided coprimes array(e) and generates private and public pair of keys. Then enter the message encrypt and decrypt. Rock and Roll!
