# Uncommon CSS `calc()` Errors

This repository demonstrates two uncommon errors that can occur when using the `calc()` function in CSS.  The first error involves omitting spaces between operators and units within the `calc()` function.  The second error shows the problem of using incompatible units in a single `calc()` expression.

## Bug 1: Missing Spaces in `calc()`

Incorrect code (bug.css):
```css
.element {width:calc(50%+10px);}
```

Corrected code (bugSolution.css):
```css
.element {width:calc(50% + 10px);}
```

## Bug 2: Incompatible Units in `calc()`

The use of incompatible units within a `calc()` expression often leads to unpredictable results. The browser struggles to convert between these units.

Incorrect code (bug.css):
```css
.element {width: calc(50% + 10em);}
```

A more compatible approach is to maintain unit consistency, or convert the units to a common base before using them inside `calc()`.

## How to Reproduce

1. Clone this repository.
2. Open `bug.html` in a web browser.
3. Observe the unexpected behavior in the rendered elements.
4. Compare with the `bugSolution.html` which shows the corrected code and expected behavior.