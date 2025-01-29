# CSS Specificity Bug

This repository demonstrates an uncommon bug in CSS related to selector specificity. The bug arises from the unexpected overriding of styles due to the specificity of selectors.

## Bug Description
The CSS file `bug.css` contains two declarations for the `.container` class. The first declaration sets the background color to lightblue. The second declaration, however, uses a more specific selector (`.container .inner`) and sets the background color to lightgreen.  Even though the first declaration comes first, the second one overrides it. This is because more specific selectors have higher precedence.

## Solution
The solution to this bug is shown in `bugSolution.css`.  A fix might include using !important flag on the less specific rule (not recommended) or changing the order (which will also work). However, the best solution is to understand how specificity works and refactor to avoid the conflict. Here we've made it clearer by removing the child selector that causes the conflict.