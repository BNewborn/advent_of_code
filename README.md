# advent_of_code
Advent of Code 2020


Tip in case I want to try automating the file download
```If you are on a linux system, or anyone else reading this, this is how my script looks like:

#!/usr/bin/env bash

# Enter your session cookie here: it's valid basically forever
cookie=<put your session cookie here, please don't mine>

[ -z $1 ] && echo "Provide the current day"    && exit 1

printf -v dirname "day_%02d" $1
mkdir "${dirname}"
curl "https://adventofcode.com/2020/day/$1/input" -s --cookie session="$cookie" > "${dirname}/input.txt"

You can get the session cookie on the AOC site by opening the developer console and navigating to where your browser stores cookies (in firefox f.e., press F12 and navigate to "Storage").
```

Code to re-use
```python 
with open('./data/day2_input.txt', 'r', newline='\n') as reader:
    input_list = reader.readlines()```
