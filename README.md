# Tcl Unexpected Error: Division by Zero in 'expr'

This repository demonstrates a subtle bug in Tcl related to division by zero within an expression used in a procedure.  The issue lies in the unexpected behavior when the denominator becomes zero due to specific input values. The lack of explicit error messaging for this scenario makes debugging more challenging.

## Bug Description:

The provided `badproc` procedure calculates 1 divided by (a-b). If 'a' and 'b' are equal, a division by zero occurs which can crash the script or provide wrong results without informative error message. The error might not be immediately apparent, particularly if the input values that lead to the problem are not obvious.

## Bug Solution:

The solution involves adding a check to prevent division by zero before the expression is evaluated.  This prevents the error from happening in the first place, leading to more robust code.