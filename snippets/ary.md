---
title: Function arity
type: snippet
tags: [function]
cover: trippy-chemicals
dateModified: 2020-10-18T20:24:28+03:00
---

Creates a function that accepts up to `n` arguments, ignoring any additional arguments.

- Call the provided function, `fn`, with up to `n` arguments, using `Array.prototype.slice()` and the spread operator (`...`).

```js
const ary = (fn, n) => (...args) => fn(...args.slice(0, n));
```

```js
const firstTwoMax = ary(Math.max, 2);
[[2, 6, 'a'], [6, 4, 8], [10]].map(x => firstTwoMax(...x)); // [6, 6, 10]
```
