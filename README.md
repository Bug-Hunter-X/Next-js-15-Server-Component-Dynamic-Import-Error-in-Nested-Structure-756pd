# Next.js 15 Server Component Dynamic Import Error

This repository demonstrates an uncommon error in Next.js 15 related to dynamic imports within deeply nested server components.  The error is an inconsistent `ReferenceError` at runtime, even when imports appear correct.  The problem is especially noticeable with hot module replacement (HMR). The solution explores strategies to reliably resolve dynamic imports in this complex scenario.

## Reproduction Steps

1. Clone the repository.
2. Install dependencies: `npm install`
3. Run the development server: `npm run dev`
4. Observe the inconsistent errors in the browser console.

## Solution

The provided solution utilizes code splitting techniques and a more explicit import strategy to consistently resolve dynamic modules across different rendering phases.  See `nestedBugSolution.js` for an effective workaround.