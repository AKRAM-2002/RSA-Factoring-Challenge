# RSA-Factoring-Challenge

## Project Overview

We have sniffed an unsecured network and found numbers that are used to encrypt very important documents. It seems that those numbers are not always generated using large enough prime numbers. Your mission should you choose to accept it, is to factorize these numbers as fast as possible before the target fixes this bug on their server - so that we can decode the encrypted documents.


## Resources

Before you begin, it's recommended to read or watch the following resources to better understand the context:

- [RSA](#)
- [How does HTTPS provide security?](#)
- [Prime Factorization](#)
- [Why RSA?](#)

## Requirements

### General

- You have the freedom to choose the programming language of your preference.
- The operating system you use must be Standard Ubuntu 20.04 LTS.

### Tasks

**Task 0: Factorize All the Things!**

- **Advanced**

Factorize as many numbers as possible into a product of two smaller numbers. To accomplish this task, you need to follow these guidelines:

- **Usage:** `factors <file>`
  - `<file>` is a text file containing natural numbers that need to be factorized.
  - Each line of the file should contain a single natural number.
  - Assume that all lines will contain valid natural numbers greater than 1.
  - There will be no empty lines, and no spaces before or after the valid number.
  - The file will always end with a new line.
  - The output format should be `n=p*q`, where `n` is the input number and `p` and `q` are the factorization results.
  - `p` and `q` don't have to be prime numbers.
  - You can work on the numbers in the file in any order.
  - Your program should run without any external dependencies. You won't be able to install anything on the machine where your program is executed.
  - There is a time limit: Your program will be terminated after 5 seconds if it doesn't complete.
  - Make sure to push all your scripts, source code, etc., to your repository.

Here's an example:

```shell
$ cat tests/test00
4
12
34
128
1024
4958
1718944270642558716715
9
99
999
9999
9797973
49
239809320265259
$ time ./factors tests/test00
4=2*2
12=6*2
34=17*2
128=64*2
1024=512*2
4958=2479*2
1718944270642558716715=343788854128511743343*5
9=3*3
99=33*3
999=333*3
9999=3333*3
9797973=3265991*3
49=7*7
239809320265259=15485783*15485773

real    0m0.009s
user    0m0.008s
sys 0m0.001s

[GitHub Repository: RSA-Factoring-Challenge](#)

## Task 1: RSA Factoring Challenge

RSA Laboratories states that for each RSA number `n`, there exist prime numbers `p` and `q` such that `n = p × q`. The challenge is to find these two prime factors when you're given only `n`. This task is similar to Task 0, with some differences:

- `p` and `q` are always prime numbers.
- There is only one number in the files.

How far can you go in less than 5 seconds? Here's how you can execute this task:

```shell
$ cat tests/rsa-1
6
$ ./rsa tests/rsa-1
6=3*2
