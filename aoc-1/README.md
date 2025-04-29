# Advent of Code 2023 - Day 1: Trebuchet?!

## Problem Description

The Elves need help with their global snow production system. They've given you a calibration document, but it's been altered by a young Elf showing off her art skills. Your task is to recover the calibration values from each line of text.

### Part 1: Finding Calibration Values

Each line contains a calibration value that can be found by combining the **first digit** and the **last digit** (in that order) to form a single two-digit number.

**Example:**
```
1abc2
pqr3stu8vwx
a1b2c3d4e5f
treb7uchet
```

In these examples:
- First line: first digit = 1, last digit = 2 → calibration value = 12
- Second line: first digit = 3, last digit = 8 → calibration value = 38
- Third line: first digit = 1, last digit = 5 → calibration value = 15
- Fourth line: first digit = 7, last digit = 7 → calibration value = 77

The sum of these calibration values (12 + 38 + 15 + 77) equals 142.

## Solution Approach

To solve this problem, you'll need to:

1. Read the input file line by line
2. For each line:
   - Find the first digit
   - Find the last digit
   - Combine them to form a two-digit number
3. Sum all the calibration values

### Algorithm Steps

1. Open and read the input file
2. Initialize a sum variable to 0
3. For each line in the input:
   - Create two pointers: one starting from the beginning (looking for the first digit) and one from the end (looking for the last digit)
   - Once both digits are found, combine them (first × 10 + last)
   - Add this value to the running sum
4. Return the final sum

## Running the Solution

1. Place your input data in a file named `input.txt`
2. Run the Python script:
   ```
   python aoc_day1.py
   ```
3. The script will output the sum of all calibration values

## Tips for Implementation

- Use character-by-character scanning to find digits
- Remember that Python has helpful built-in methods like `isdigit()` to check if a character is a digit
- Consider edge cases where a line might have only one digit (in this case, it would be both the first and last digit)
- Proper file handling with context managers (`with open...`) ensures files are closed appropriately

Good luck with your Advent of Code challenge!
