# JavaScript Loose Equality Bug

This repository demonstrates a common, yet subtle bug in JavaScript related to loose equality (==) when performing addition.  The `foo` function intends to add two numbers, handling `null` or `undefined` gracefully. However, due to the use of loose equality, unexpected behavior may occur.

## Bug Description
The primary issue lies in the use of `==` within the `if` condition.  Loose equality performs type coercion, leading to unexpected results in certain scenarios. For instance, `0 == false` evaluates to `true`, which is not always desired when checking for `null` or `undefined` explicitly.

## How to Reproduce
1. Clone this repository.
2. Run the `bug.js` file using a JavaScript runtime (e.g., Node.js).
3. Observe the outputs. You'll notice unexpected results due to loose equality handling of null and undefined values.

## Solution
The solution involves replacing the loose equality (==) with strict equality (===). Strict equality avoids type coercion, providing more predictable results.

## Solution Code
The corrected code uses strict equality (===), resolving the loose equality issues and ensuring more predictable behavior when handling `null` or `undefined` inputs.
