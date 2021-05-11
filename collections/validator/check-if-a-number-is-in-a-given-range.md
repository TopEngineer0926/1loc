---
title: Check if a number is in a given range
category: Validator
tags:
  - posts
layout: layouts/post.njk
---

```js
const inRange = (num, a, b, threshold = 0) => (Math.min(a, b) - threshold <= num && num <= Math.max(a, b) + threshold);

// Example
inRange(10, 5, 15);         // true
inRange(10, 5, 6);          // false
inRange(10, 15, 5);         // true
inRange(-10, -5, -15);      // true
```