[![](https://www.ginar.io/wp-content/themes/ginar/assets/img/logo1.svg)](https://ginar.io)
# Statistical test
[![](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://github.com/ginarteam) [![](https://img.shields.io/badge/Telegram-Group-blue.svg)](https://t.me/GINAR_io) 


GINAR is a blockchain technology company specializing in providing a decentralized random number generator. Random Number Generation, or RNG, is a key component to applications that benefit from true randomness. GINAR is set to release a best-in-class decentralized.
- Random Number Generator (dRNG) that will change the financial, gambling, online gaming, and IOT industry by providing the fastest, most secure and easily verifiable service, ..

- For more detail about GINAR: Read our white-paper -> [![](https://img.shields.io/badge/docs-latest-af1a97.svg)](https://www.ginar.io/whitepaper-v2.0.pdf)

This is result of Dieharder statistical test suite for Random Number Generator (RNG) that apply to GINAR RNG    

# Dieharder Statistical Test Suite

  
> Diehard tests are a battery of statistical tests for measuring the quality of a random
number generator. It contains 16 statistical tests. This battery was developed by George
Marsaglia over several years and first published in 1995. It is a complete, thorough and
comprehensive set of statistical tests for PRNG. This set of statistical tests serves as
some kind of litmus for checking and eventual certification of PRNG. If a PRNG
passes Diehard statistical tests, then it can be used in more serious scientific researches.

[Diehard Statistical Test Suite](https://web.archive.org/web/20160125103112/http://stat.fsu.edu/pub/diehard/)

### Installation
You can install dieharder test suite directly from Linux Package Managesment. 
(Ubuntu)
```sh
$ sudo apt-get install dieharder
```

### Get data for random test

You need a dataset of random number for the test. We have built a function that help you get data from GINAR:
- Login your account  GINAR
- Initialize your session key
- Copy the init-session-key link (url)

This test suite requires a lot of numbers. We recommend using 30.000.000 numbers.

Or you can get the sample of random number that we provide on github.
- Clone the repository or just download zip file and all extended file (archive.*).
- unzip the file and you will get input.bin (the random-number-file gotten from GINAR).

### Run the test
```sh
$ dieharder -d {0-16} -g 202 -f input.bin [-D default -D histogram]
```

### Output and visualization

You can read the result in output2.txt on github or read output of the test suite when you run the command above.

Sample of `result`:

```
#=============================================================================#
#            dieharder version 3.31.1 Copyright 2003 Robert G. Brown          #
#=============================================================================#
   rng_name    |           filename             |rands/second|
     file_input|                       input.bin|  6.03e+06  |
#=============================================================================#
#                         Histogram of test p-values                          #
#=============================================================================#
# Bin scale = 0.100000
#     20|    |    |    |    |    |    |    |    |    |    |
#       |    |    |    |    |    |    |    |    |    |    |
#     18|    |    |    |    |    |    |    |    |    |    |
#       |    |    |    |    |    |    |    |    |    |    |
#     16|    |    |    |    |    |    |    |    |    |    |
#       |    |    |    |    |    |    |    |    |    |    |
#     14|    |    |    |    |    |    |    |    |    |    |
#       |    |****|    |    |    |****|    |    |    |****|
#     12|    |****|****|    |    |****|    |    |    |****|
#       |    |****|****|    |    |****|****|    |    |****|
#     10|    |****|****|    |    |****|****|    |    |****|
#       |****|****|****|****|    |****|****|    |    |****|
#      8|****|****|****|****|    |****|****|    |****|****|
#       |****|****|****|****|    |****|****|****|****|****|
#      6|****|****|****|****|    |****|****|****|****|****|
#       |****|****|****|****|****|****|****|****|****|****|
#      4|****|****|****|****|****|****|****|****|****|****|
#       |****|****|****|****|****|****|****|****|****|****|
#      2|****|****|****|****|****|****|****|****|****|****|
#       |****|****|****|****|****|****|****|****|****|****|
#       |--------------------------------------------------
#       | 0.1| 0.2| 0.3| 0.4| 0.5| 0.6| 0.7| 0.8| 0.9| 1.0|
#=============================================================================#
#=============================================================================#
        test_name   |ntup| tsamples |psamples|  p-value |Assessment
#=============================================================================#
   diehard_birthdays|   0|       100|     100|0.89925936|  PASSED  

```

