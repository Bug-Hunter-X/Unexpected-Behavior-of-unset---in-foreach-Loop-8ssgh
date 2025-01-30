# PHP Foreach Loop and unset() Bug
This repository demonstrates a subtle bug related to using `unset()` within a `foreach` loop in PHP. Modifying the array being iterated over within the loop can lead to unexpected behavior due to the way PHP handles array indices.

## Problem
The provided PHP code aims to remove elements with the value 'bar' from an array.  However, when multiple 'bar' values exist, `unset()` causes index shifting, leading to elements being skipped.

## Solution
The solution uses `array_filter()` to achieve a cleaner and more predictable way to remove elements. `array_filter` doesn't modify the original array during iteration.