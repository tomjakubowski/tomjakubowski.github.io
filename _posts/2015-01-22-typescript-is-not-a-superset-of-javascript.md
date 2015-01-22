---
layout: post
title: TypeScript is not a superset of JavaScript
tags: typescript pedantry

---

I've seen this claim made all over the place but it's not true. From [Wikipedia][wiki]:

> TypeScript is a strict superset of JavaScript. As such, a JavaScript program
> is also a valid TypeScript program, and a TypeScript program can seamlessly
> consume JavaScript. TypeScript compiles to ES3-compatible JavaScript.

And from the [TypeScript website][ts]:

> TypeScript is a typed superset of JavaScript that compiles to plain JavaScript.
> … With TypeScript, you can use existing JavaScript code, incorporate popular
> JavaScript libraries, and be called from other JavaScript code.

As a counterexample consider this simple JavaScript program:

```javascript
function foo() { }
foo(1);
```

which is an illegal TypeScript program:

```
foo.ts(2,1): error TS2346: Supplied parameters do not match any signature
of call target.
```

[wiki]: <http://en.wikipedia.org/wiki/TypeScript#Compatibility_with_JavaScript>
[ts]: <http://www.typescriptlang.org/>
