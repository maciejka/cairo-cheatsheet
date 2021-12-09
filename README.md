# Cairo Cheatsheet

<img src="/assets/icon.png" width="50">

## Arithmetics
```python
from starkware.cairo.common.math import (assert_in_range, assert_le, ...)

# Field operations.
(a + b * c) / d
assert_not_zero(a)
# Assert 0 <= a < 2**128.
assert_nn(a)
# Assert 0 <= b - a < 2**128.
assert_le(a, b)
# Assert 0 <= a < b, 2**128.
assert_nn_le(a, b)
# Assert a <= b (as numbers between 0 and PRIME - 1).
assert_le_felt(a, b)
# Compute the quotient and remainder when integer dividing a by b.
# Assumes 0 <= b < 2**120, and a < 2**128 * div.
let (q, r) = unsigned_div_rem(a, b)
# Note: signed_div_rem treats a as a signed number.
```