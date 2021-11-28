# **CE4010 Course Project**

## Topic #8: Demonstration of Attacks on "Weak" RSA

<br>

The objective of the project is to implement a simple, practical RSA protocol that has a weak implementation and demonstrate an attack on the protocol to recover either the key or plaintext.

This project serves as an interactive demonstrator, allowing users to provide their own plaintext inputs to see how the plaintext can be recovered from the ciphertexts without using the private decryption exponent. It showcases three different types of RSA attacks to recover the original plaintext:

<ol>
<li>Low Public Exponent Attack</li>
<li>Hastad Broadcasting Attack</li>
<li>Common Modulus Attack</li>
</ol>

The project was created using Python on Jupyter Notebook, and rendered as a web application using Binder. Please use the following Binder link to view the project:

https://mybinder.org/v2/gh/chian95/ce4010-course-proj/HEAD?urlpath=%2Fvoila%2Frender%2FRSADemo.ipynb

Please note that Binder may take some time to load, and upon reaching the main page, the buttons for viewing other sections may appear only after a few seconds.

<br>

---

## Research and Design

<br>

Research was done to find suitable modules/packages to simplify some of the mathematical computations required for the RSA attacks. For example, the `modint` package was used to obtain the solution for the Chinese Remainder Theorem (CRT) in the demonstration for the Hastad Broadcasting Attack; it was able to obtain solutions for very large numbers quickly and efficiently without any issues as compared to some of the other packages I have tried using.

For the project design, I wanted to make the notebook more like a web application, as a web application will be more interactive and intuitive for the users with the usage of buttons and text fields, and it has a less linear structure as compared to the conventional notebook.

<br>

---

## Development/Implementation

<br>

To implement a practical RSA protocol, I used the built-in `decimal` module which allows for user defined precision to increase the precision of the numbers so that decimal floating point arithmetic for very large integers can be performed. In this way, longer plaintexts can be encrypted into ciphertexts of very large values but they can still be cracked.

In addition, for the increased interactivity of the demonstrator, interactive widgets were implemented in order to have the notebook rendered as a web application.

<br>

---

## References

<br>

[1] https://www.members.tripod.com/irish_ronan/rsa/attacks.html

[2] https://www.utc.edu/sites/default/files/2021-04/course-paper-5600-rsa.pdf

[3] https://thescipub.com/pdf/jcssp.2006.665.671.pdf

[4] https://infosecwriteups.com/rsa-attacks-common-modulus-7bdb34f331a5