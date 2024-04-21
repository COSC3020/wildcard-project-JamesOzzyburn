[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/tTztJ7yI)
# Wildcard Project

You have a cool idea for an algorithms project? Use this repository. Make sure
to explain what problem you're solving, how you're doing it, and that you test
your code.


## Project Description
For my wildcard project I decided to try to compare the runtime of different languages namely JavaScript and Python (I also used ChatGPT to convert the code into c++ as well, just to how well an AI would write code). For the code in my project, I started out by taking my tsp held karp implementation and adding a timing function at the end that ran a through a fixed set of matrices 10 times each and then calculated the average. I made matrices with city sizes of 10-19 as those are the ones in my testing that ran in a reasonable amount of time. For my runtime tests, I ran it on my own laptop through wsl2 running Ubuntu. 

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
root@James-Windows:/home/nick/testing_algo/wildcard# g++ -o code code.cpp
root@James-Windows:/home/nick/testing_algo/wildcard# ./code
Running Held Karp
10 cities in 0.08858090 seconds on average
11 cities in 0.23183990 seconds on average
12 cities in 0.61720220 seconds on average
13 cities in 1.61320670 seconds on average
14 cities in 3.93221660 seconds on average
15 cities in 9.67804750 seconds on average
16 cities in 23.76998470 seconds on average
17 cities in 57.66779610 seconds on average
18 cities in 147.18429010 seconds on average
19 cities in 333.78606780 seconds on average
```

### C++ run with compiler optimizations
```
root@James-Windows:/home/nick/testing_algo/wildcard# g++ -O3 -o codeOP code.cpp
root@James-Windows:/home/nick/testing_algo/wildcard# ./codeOP
Running Held Karp
10 cities in 0.00909280 seconds on average
11 cities in 0.02394440 seconds on average
12 cities in 0.06400930 seconds on average
13 cities in 0.17167340 seconds on average
14 cities in 0.52317970 seconds on average
15 cities in 1.28748770 seconds on average
16 cities in 3.34501490 seconds on average
17 cities in 7.67311960 seconds on average
18 cities in 17.36208340 seconds on average
19 cities in 44.70391720 seconds on average
```

### Final Thoughts
It seems that the time difference between python, node, and c++ with optimizations is pretty small all things considered. The fascinating part I think is how badly the AI converted code ran, and that is also after I had to spend ~2 hours fixing the code it gave me by telling it the errors the build produced. So it really proves that once again that even with a fast language such a c++ if you give it bad code or poorly written code it's going to run very poorly. Also, it shows that compiler optimizations are very cool and a very easy way to potentially “save/fix” very slow code.
