# The Discrete Logarithm Problem : 
### The Hidden Mathematics Behind Digital Security 

## Introduction 
Exploring the Mathematics, Computational Complexity, and Cryptographic Applications Behind One of the Most Important Problems in Modern Cryptography.
What was the problem ?
We had Standard Symmetric Encryption Systems but the main problem is to exchange the keys to decrypt the encryption which is encrypted in Symmetric Encrytion Algorithms. Some on can say we had Public Key Encryption but the problem while using Public Key Encryption is :

    1. Computational Overload :- Asymmetric mathematics uses massive numbers and complex modular  arithmetic.

    2. File Size and Speed Limits :- Data size is mathematically limited by the key size, making it much slower than bulk symmetric encryption.

    3. Man in the Middle Attacks 

    4. Identity Verification Challenges

    5. Private Key Loss or compromise

    6. Quantum Computing Threats

    7. Key Mismanagement and Expiration

so we need a reliable solution to exchange keys and it must be mathematically infeasible to decode the algorithm. 
solution for this problem is to implement Discrete Logarithm Problem which is mainly applicable in :

    1. Diffie Hellman Key Exchange - Helps two parties establish a shared secret over a public channel.

    2. Digital Signature Algorithm(DSA) - provides the mathematical foundation for signature security.

    3. Bitcoin & Ethereum - ECDSA(Elliptic Curve Digital Signature Algorithm) rely on the elliptic curve discrete logarithm problem.

    4. Secure Communication - Discrete logarithm based key agreement can help establish keys for encrypted communication.

    etc.....

## Mathematical Representation and Working of DLP
The Discrete Logarithm Problem (DLP) is a mathematical problem where you must find an unknown exponent x in a modular or group equation of the form:

$g^x \equiv h \pmod p$

where, 

<p>'g' is generator
'h' is known number
'p' is prime number
'x' is unknown</p>

#### Example : 
$$ 2^x \equiv 9 \pmod{11} $$ , find x ?

Testing for 'x' values :
$$ 2^1 \equiv 2 \pmod{11} $$
$$ 2^2 \equiv 4 \pmod{11} $$
$$ 2^3 \equiv 8 \pmod{11} $$
$$ 2^4 \equiv 5 \pmod{11} $$
$$ 2^5 \equiv 10 \pmod{11} $$
$$ 2^6 \equiv 9 \pmod{11} $$

The solution is x = 6 which satisfies DLP. With small numbers, trial multiplication works quickly, but for large primes, it becomes practically impossible

Until we know only how to solve the Discrete Logarithm Problem it's basically we need to solve for x in Cyclic Field ($g^x = h$). So Now lets go to the main use cases of DLP , for this magazine we will be looking only DLP applications for Secure Key Exchange Protocol(i.e, DHKE) and Digital Signature (i.e,ECDSA)

## Diffie - Hellman Key Exchange (DHKE)
### Overview
#### What is Diffie Hellman Key Exchange?
    Diffie Hellman Key Exchange is a technique that allows two perties to establish a shared secret over a public channel without directly transmitting the secret itself.


### Mathematical

##### General working of shared secret using DLP
The Values of g and p are public which they can choose by two parties
###### Party 1 :
$$A = g^a \mod p $$
The value of A is sent to party 2 by party 1 to calculate the shared key

###### Party 2 :
$$B = g^b \mod p $$
The value of B is sent to party 1 by party 2 to calculate the shared key

###### Calculate for Shared Key :
###### For Party 1:
$$K = B^a \mod p $$
###### For Party 2:
$$K = A^b \mod p $$

The values of both K are equal that is the shared key between party 1 and party 2 

## Elliptic Curve Digital Signature Algorithm (ECDSA)

### Overview
#### What is ECDSA ?
    Elliptic Curve Digital Signature Algorithm is a digital signature algorithm that uses Elliptic Curve Cryptography.

### Mathematical

The discrete logarithm problem is defined as $g^x \equiv y \pmod p$.

## Why Discrete Logarithm Problem is hard to revert 
### Overview
### Mathematical



## Attacking Research
### Overview 
### code



## Conlusion 





