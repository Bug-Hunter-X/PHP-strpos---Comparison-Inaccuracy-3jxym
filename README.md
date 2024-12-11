# PHP strpos() Comparison Inaccuracy
This repository demonstrates a common yet subtle error when using the `strpos()` function in PHP.  The issue arises from PHP's loose typing and the fact that `strpos()` returns `0` (falsy) when the needle is found at the very beginning of the haystack, leading to unexpected results when comparing its return value to `false` using strict comparison (`===`).

The `bug.php` file shows the problematic code, while `bugSolution.php` provides the corrected version. The core problem is accurately checking if the needle is *not* found using strict comparison of the function's output with `false`.

This example highlights the importance of careful type handling and using strict comparison operators in PHP to avoid such common pitfalls.