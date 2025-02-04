---
title: Byte size of string
type: snippet
tags: [string]
cover: mountain-lake-cottage-2
dateModified: 2020-10-18T23:04:45+03:00
---

Returns the length of a string in bytes.

- Convert a given string to a [`Blob` Object](https://developer.mozilla.org/en-US/docs/Web/API/Blob).
- Use `Blob.size` to get the length of the string in bytes.

```js
const byteSize = str => new Blob([str]).size;
```

```js
byteSize('😀'); // 4
byteSize('Hello World'); // 11
```
