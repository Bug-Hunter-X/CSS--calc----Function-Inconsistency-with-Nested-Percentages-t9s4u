# CSS `calc()` Function Inconsistency with Nested Percentages

This repository demonstrates a subtle bug related to the CSS `calc()` function and its interaction with nested percentage values.  The bug manifests primarily when using percentages within `calc()` in situations with dynamic or changing parent element sizes, especially those involving scrolling content.

The issue is that `calc()`'s interpretation of nested percentage values isn't always consistent, leading to unpredictable sizing of elements, particularly for heights. This inconsistency becomes more prominent in layouts where the parent container's height depends on its content rather than a fixed value.

The `bug.css` file contains the problematic code.  The `bugSolution.css` file proposes a possible workaround or alternative solution.

## Reproducing the Bug

1. Clone this repository.
2. Open `bug.html` (not included, but you can easily create one with the `bug.css` styles applied to an element).
3. Observe the unexpected behavior in different scenarios (e.g., changing the content of the parent container).

## Solution

The provided solution in `bugSolution.css` may involve using alternative layout techniques, such as flexbox or grid, which have more robust handling of dynamic sizing.  Alternatively, avoid nested percentage-based calculations within `calc()` when possible, opting for fixed values or javascript calculations to ensure consistent and predictable results.