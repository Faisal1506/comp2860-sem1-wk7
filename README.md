# COMP2860 Semester 1 Week 7 Exercises.

## Exercise 1: Shift Cipher
For the shift cipher, the mathematical formula for encryption with a forward shift is

$C = P + K \pmod{26}$

where $P$ is the plaintext letter (represented as a number from 0 to 25), $C$ is the ciphertext letter (represented as a number from 0 to 25) and $K$ is the shift (a number from 0 to 25). $\bmod$ is the modulo operation which gives the remainder after dividing the preceding number by the following number. For example, if $P=24$ (Y) and $K=3$, then $P+K=27$. $27\bmod{26}=1$ because 26 divides 27 once with remainder 1. 1 corresponds to the letter B.

Similarly, the mathematical formula for decryption with a backward shift is

$P = C − K \pmod{26}$

Using the above formulae, open ```exercise1.py``` and complete the ```ShiftCipher``` class by implementing the following class methods. Descriptions of what each method should do, its parameters and return value are given in the comments.

1. ```__shift_letter``` which performs a forward or backward shift of a letter. (Hint: ```%``` is the Python modulo operator. The built-in Python functions ```ord``` and ```chr``` may help you convert letters to numbers and vice versa.)
2. ```encrypt```
3. ```decrypt```

Unit tests for the ```encrypt``` and ```decrypt``` methods are provided for you. They are located in ```test_exercise1.py```.

## Exercise 2: Cryptanalysis of Shift Cipher
Open ```exercise2.py``` and complete the Python script so that it performs exhaustive key search on a ciphertext
encrypted using the shift cipher.

## Exercise 3: Simple Substitution Cipher
Open ```exercise3.py``` and complete the ```SubstitutionCipher``` class by implementing the following class methods. Descriptions of what each method should do, its parameters and return value are given in the comments.
1. ```encrypt```
2. ```decrypt```

Unit tests for the ```encrypt``` and ```decrypt``` methods are provided for you. They are located in ```test_exercise3.py```.

## Exercise 5: Vigenere Cipher (Portfolio Task)
Open ```exercise5.py``` and complete the ```VigenereCipher``` class by implementing the following class methods. Descriptions of what each method should do, its parameters and return value are given in the comments.

Do not change method names, method parameter lists or method return values. Otherwise, the automated marking in Gradescope will fail.

1. ```__shift_letter``` which performs a forward or backward shift of a letter. (Hint: You should be able to reuse your code for the method of the same name from exercise 1 with minor modifications).
2. ```__generate_shift_list```. This function generates a string by repeating keyword for as many letters as supplied in the parameter ```num_letters```. (Note: ```num_letters``` may not be an exact multiple of the number of letters in the keyword.) It should then convert each letter in the string to a number from 0 (A) to 25 (Z), and output the set of shifts as a list of numbers.
3. ```encrypt```
4. ```decrypt```

Unit tests for the ```encrypt``` and ```decrypt``` methods are provided for you. They are located in ```test_exercise5.py```.
