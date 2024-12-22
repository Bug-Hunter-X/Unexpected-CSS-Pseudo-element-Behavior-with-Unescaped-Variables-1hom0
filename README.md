# Unexpected CSS Pseudo-element Behavior with Unescaped Variables
This repository demonstrates a subtle bug in CSS involving the use of unescaped variables or expressions within the `content` property of pseudo-elements (::before, ::after).  The problem arises when the variable or expression contains characters that conflict with CSS syntax, leading to unexpected rendering or parsing errors.

## Bug Description
The core issue is that if a variable or expression used in a pseudo-element's `content` property contains unescaped special characters (e.g., quotes, parentheses, or other CSS-significant characters), the CSS parser might misinterpret the content, truncating it prematurely or throwing unexpected errors.

## Solution
The solution involves proper escaping of any variable or expression that may contain potentially problematic characters.  This ensures that the CSS parser treats them as literal parts of the string rather than as syntax elements.

## How to Reproduce
1. Open `bug.css`.
2. Observe the unexpected rendering of the pseudo-element content in your browser.
3. Open `bugSolution.css`.
4. Observe how proper escaping solves the problem.