# Tailwind CSS @apply Directive Bug with Custom Directives

This repository demonstrates a bug where Tailwind CSS's `@apply` directive does not work correctly when used with custom classes within custom directives.  The `@apply` directive is expected to apply the specified class to the element. However, this fails when the class is a custom utility, defined within the custom directive.

## Bug Reproduction

1. Clone this repository.
2. Open `bug.html` in a browser.
3. Observe that the `div` element does not have the expected styles applied (red background, padding).

## Solution

The solution is to avoid using `@apply` with custom classes and instead directly apply the styles. Alternatively, define the custom styles in a separate stylesheet and include them in your main stylesheet. See `bugSolution.html` for the corrected version.

## Additional Notes

This issue is specific to `@apply` and custom directives. Using `@apply` with standard Tailwind classes works as expected.