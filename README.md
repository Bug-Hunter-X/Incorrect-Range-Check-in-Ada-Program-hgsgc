# Ada Range Check Bug

This repository demonstrates a common error in Ada programs involving range checks. The program is intended to check if an integer is within the range [10, 20]. However, due to a logical error, the result is incorrect when the input number is less than 10.  The solution shows the correct way to implement the range check.

## Bug Description
The `Check_Range` function does not correctly handle numbers less than 10. The current implementation results in unexpected behavior for this case. The `and` operator short-circuits and doesn't check the second condition when the first is false.  This makes the function return `false` even if the number is less than 10, but greater than 20, which is incorrect.

## Solution
The solution clarifies the range check condition and uses appropriate logical operators to ensure the range is checked correctly, handling numbers less than 10 appropriately.