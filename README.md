rollup-bug
==========

This repo has been setup with:
- `npm init`
- `npm install --save-dev jspm@0.17.0-beta.47`
- `jspm init`

And contains a single ES module (`index.js`) with an object as such:

```
export const testObj = {
  async: true
};
```

Running `jspm build index.js` generates the following error:

```
laurent@MacBook-Pro rollup-bug [master] $ jspm build index.js
     Creating the single-file build for index.js...

err  SyntaxError: Unexpected token (2:7) in index.js
    at Parser.pp$4.raise (/Users/laurent/Development/freelancer/rollup-bug/node_modules/rollup/dist/rollup.js:4070:13)
    at Parser.pp.unexpected (/Users/laurent/Development/freelancer/rollup-bug/node_modules/rollup/dist/rollup.js:2268:8)
    at Parser.pp$3.parseIdent (/Users/laurent/Development/freelancer/rollup-bug/node_modules/rollup/dist/rollup.js:4029:10)
    at Parser.pp$3.parsePropertyName (/Users/laurent/Development/freelancer/rollup-bug/node_modules/rollup/dist/rollup.js:3874:121)
    at Parser.pp$3.parseObj (/Users/laurent/Development/freelancer/rollup-bug/node_modules/rollup/dist/rollup.js:3802:14)
    at Parser.pp$3.parseExprAtom (/Users/laurent/Development/freelancer/rollup-bug/node_modules/rollup/dist/rollup.js:3605:17)
    at Parser.pp$3.parseExprSubscripts (/Users/laurent/Development/freelancer/rollup-bug/node_modules/rollup/dist/rollup.js:3492:19)
    at Parser.pp$3.parseMaybeUnary (/Users/laurent/Development/freelancer/rollup-bug/node_modules/rollup/dist/rollup.js:3469:17)
    at Parser.pp$3.parseExprOps (/Users/laurent/Development/freelancer/rollup-bug/node_modules/rollup/dist/rollup.js:3411:19)
    at Parser.pp$3.parseMaybeConditional (/Users/laurent/Development/freelancer/rollup-bug/node_modules/rollup/dist/rollup.js:3394:19)
    at Parser.pp$3.parseMaybeAssign (/Users/laurent/Development/freelancer/rollup-bug/node_modules/rollup/dist/rollup.js:3371:19)
    at Parser.pp$1.parseVar (/Users/laurent/Development/freelancer/rollup-bug/node_modules/rollup/dist/rollup.js:2728:26)
    at Parser.pp$1.parseVarStatement (/Users/laurent/Development/freelancer/rollup-bug/node_modules/rollup/dist/rollup.js:2611:8)
    at Parser.pp$1.parseStatement (/Users/laurent/Development/freelancer/rollup-bug/node_modules/rollup/dist/rollup.js:2396:17)
    at Parser.pp$1.parseExport (/Users/laurent/Development/freelancer/rollup-bug/node_modules/rollup/dist/rollup.js:2894:29)
    at Parser.pp$1.parseStatement (/Users/laurent/Development/freelancer/rollup-bug/node_modules/rollup/dist/rollup.js:2409:69)
```
