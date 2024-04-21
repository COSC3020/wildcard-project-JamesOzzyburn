[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/tTztJ7yI)
# Wildcard Project

You have a cool idea for an algorithms project? Use this repository. Make sure
to explain what problem you're solving, how you're doing it, and that you test
your code.


## Project Description
For my wildcard project I decided to try and compare the runtime of different languages namly javascript and python (I also used chatgpt to convert the code into c++ as well, just to how well an ai would write code). For the first part of my project so I started out by first taking my tsp held karp implementation and adding a timing function at the end that ran a through a fixed set of matricies 10 times each and then calculated the average. I made matricies with city sizes of 10-19 as those are the ones in my testing that ran in a reasonable amount of time. For my runtime tests I ran it on my own laptop thriugh wsl2 using Ubuntu. 

### Node run
```
root@James-Windows:/home/nick/testing_algo/wildcard# node code.js
Running Held Karp
10 cities in 0.01460000 seconds on average
11 cities in 0.03170000 seconds on average
12 cities in 0.07650000 seconds on average
13 cities in 0.18930000 seconds on average
14 cities in 0.45630000 seconds on average
15 cities in 1.11770000 seconds on average
16 cities in 2.69810000 seconds on average
17 cities in 6.33830000 seconds on average
18 cities in 15.16460000 seconds on average
19 cities in 35.21300000 seconds on average
```

### Python run
```
root@James-Windows:/home/nick/testing_algo/wildcard# python3 pycode.py
Running Held Karp
10 cities in 0.01972353 seconds on average
11 cities in 0.04794586 seconds on average
12 cities in 0.12224712 seconds on average
13 cities in 0.30389297 seconds on average
14 cities in 0.73808115 seconds on average
15 cities in 1.78737695 seconds on average
16 cities in 4.23764100 seconds on average
17 cities in 9.93840678 seconds on average
18 cities in 23.29102845 seconds on average
19 cities in 54.40469213 seconds on average
```

### C++ run with no optimizations
```

```

### C++ run with compiler optimizations
```

```
