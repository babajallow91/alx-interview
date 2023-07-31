
<<<<<<< HEAD
# 0x05. N Queens
=======
# 0x03. Log Parsing
>>>>>>> f16f7960a3cdbe62155c8e44bfc25ca95ace4586



## Requirements

### General

-   Allowed editors: `vi`, `vim`, `emacs`
-   All your files will be interpreted/compiled on Ubuntu 14.04 LTS using `python3` (version 3.4.3)
-   All your files should end with a new line
-   The first line of all your files should be exactly `#!/usr/bin/python3`
-   A `README.md` file, at the root of the folder of the project, is mandatory
<<<<<<< HEAD
-   Your code should use the `PEP 8` style (version 1.7.\*)
-   All your files must be executable

## Tasks

### 0\. N queens

mandatory

![](http://www.crestbook.com/files/Judit-photo1_602x433.jpg)  
Chess grandmaster [Judit Polgár](https://en.wikipedia.org/wiki/Judit_Polg%C3%A1r), the strongest female chess player of all time  
  

The N queens puzzle is the challenge of placing N non-attacking queens on an N×N chessboard. Write a program that solves the N queens problem.

-   Usage: `nqueens N`
    -   If the user called the program with the wrong number of arguments, print `Usage: nqueens N`, followed by a new line, and exit with the status `1`
-   where N must be an integer greater or equal to `4`
    -   If N is not an integer, print `N must be a number`, followed by a new line, and exit with the status `1`
    -   If N is smaller than `4`, print `N must be at least 4`, followed by a new line, and exit with the status `1`
-   The program should print every possible solution to the problem
    -   One solution per line
    -   Format: see example
    -   You don’t have to print the solutions in a specific order
-   You are only allowed to import the `sys` module

Read: [Queen](https://en.wikipedia.org/wiki/Queen_%28chess%29), [Backtracking](https://en.wikipedia.org/wiki/Backtracking)

```
julien@ubuntu:~/0x08. N Queens$ ./0-nqueens.py 4
[[0, 1], [1, 3], [2, 0], [3, 2]]
[[0, 2], [1, 0], [2, 3], [3, 1]]
julien@ubuntu:~/0x08. N Queens$ ./0-nqueens.py 6
[[0, 1], [1, 3], [2, 5], [3, 0], [4, 2], [5, 4]]
[[0, 2], [1, 5], [2, 1], [3, 4], [4, 0], [5, 3]]
[[0, 3], [1, 0], [2, 4], [3, 1], [4, 5], [5, 2]]
[[0, 4], [1, 2], [2, 0], [3, 5], [4, 3], [5, 1]]
julien@ubuntu:~/0x08. N Queens$ 
=======
-   Your code should use the `PEP 8` style (version 1.7.x)
-   All your files must be executable
-   The length of your files will be tested using `wc`

## Tasks

### 0\. Log parsing

mandatory

Write a script that reads `stdin` line by line and computes metrics:

-   Input format: `<IP Address> - [<date>] "GET /projects/260 HTTP/1.1" <status code> <file size>` (if the format is not this one, the line must be skipped)
-   After every 10 lines and/or a keyboard interruption (`CTRL + C`), print these statistics from the beginning:
    -   Total file size: `File size: <total size>`
    -   where `<total size>` is the sum of all previous `<file size>` (see input format above)
    -   Number of lines by status code:
        -   possible status code: `200`, `301`, `400`, `401`, `403`, `404`, `405` and `500`
        -   if a status code doesn’t appear or is not an integer, don’t print anything for this status code
        -   format: `<status code>: <number>`
        -   status codes should be printed in ascending order

**Warning:** In this sample, you will have random value - it’s normal to not have the same output as this one.

```
alexa@ubuntu:~/0x03-log_parsing$ cat 0-generator.py
#!/usr/bin/python3
import random
import sys
from time import sleep
import datetime

for i in range(10000):
    sleep(random.random())
    sys.stdout.write("{:d}.{:d}.{:d}.{:d} - [{}] \"GET /projects/260 HTTP/1.1\" {} {}\n".format(
        random.randint(1, 255), random.randint(1, 255), random.randint(1, 255), random.randint(1, 255),
        datetime.datetime.now(),
        random.choice([200, 301, 400, 401, 403, 404, 405, 500]),
        random.randint(1, 1024)
    ))
    sys.stdout.flush()

alexa@ubuntu:~/0x03-log_parsing$ ./0-generator.py | ./0-stats.py 
File size: 5213
200: 2
401: 1
403: 2
404: 1
405: 1
500: 3
File size: 11320
200: 3
301: 2
400: 1
401: 2
403: 3
404: 4
405: 2
500: 3
File size: 16305
200: 3
301: 3
400: 4
401: 2
403: 5
404: 5
405: 4
500: 4
^CFile size: 17146
200: 4
301: 3
400: 4
401: 2
403: 6
404: 6
405: 4
500: 4
Traceback (most recent call last):
  File "./0-stats.py", line 15, in <module>
Traceback (most recent call last):
  File "./0-generator.py", line 8, in <module>
    for line in sys.stdin:
KeyboardInterrupt
    sleep(random.random())
KeyboardInterrupt
alexa@ubuntu:~/0x03-log_parsing$ 
>>>>>>> f16f7960a3cdbe62155c8e44bfc25ca95ace4586
```

**Repo:**

-   GitHub repository: `alx-interview`
<<<<<<< HEAD
-   Directory: `0x05-nqueens`
-   File: `0-nqueens.py`
=======
-   Directory: `0x03-log_parsing`
-   File: `0-stats.py`
>>>>>>> f16f7960a3cdbe62155c8e44bfc25ca95ace4586
