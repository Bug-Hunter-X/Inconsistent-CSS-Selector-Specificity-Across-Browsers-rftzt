# Inconsistent CSS Selector Specificity

This repository demonstrates a common issue with CSS selector specificity, where a more specific selector is unexpectedly overridden by a less specific one due to inconsistencies in how different browsers interpret and apply CSS rules.  The problem manifests in inconsistent styling across browsers.

## Problem

The provided CSS code contains two selectors: `div p` and `p`.  While `div p` is more specific, some browsers might unexpectedly prioritize the `p` selector, leading to unexpected styling.  This is largely due to the intricacies of how browsers handle cascading and selector specificity, which are not always perfectly consistent across different rendering engines.

## Solution

The solution involves several strategies to ensure the intended styling: 

1. **Increase Specificity:** Add more specific selectors to `div p` to make it even more dominant.
2. **Order of Rules:** Ensure the rules are ordered to reflect intended cascade. The more specific rules should always come later to ensure they always override less specific rules. 
3. **Avoid Ambiguity:**  Carefully review your selectors and make them more explicit. Avoid the use of ambiguous selectors whenever possible.

By implementing one of these solutions, consistent and predictable styling can be achieved across different browsers.  This repository contains example CSS code illustrating the problem and demonstrates the effectiveness of the proposed solutions.