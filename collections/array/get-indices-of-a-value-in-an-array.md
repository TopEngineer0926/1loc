---
title: Get indices of a value in an array
category: Array
tags:
  - posts
layout: layouts/post.njk
---

```js
const indices = (arr, value) => arr.reduce((acc, v, i) => (v === value ? [...acc, i] : acc), []);

// Or
const indices = (arr, value) => arr.map((v, i) => v === value ? i : false).filter(Boolean);

// Examples
indices(['h', 'e', 'l', 'l', 'o'], 'l');    // [2, 3]
indices(['h', 'e', 'l', 'l', 'o'], 'w');    // []
```