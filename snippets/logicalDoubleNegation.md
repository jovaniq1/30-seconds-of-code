---
title: Logical Double Negation
tags: function
expertise: beginner
cover: blog_images/blue-bird.jpg
firstSeen: 2022-08-22T05:00:00-04:00
---

Explanation on how double negation works and their return on certain values.

- Given a boolean, ! will negate the value. Having a value other than a boolean, the value will first be converted to a boolean and then negated.
- Having a double negations will automatically yield false for a value like !!undefined.

```js
const singleNegation = (array) => array.map((val) => !val);
```

```js
const doubleNegation = (array) => array.map((val) => !!val);
```

```js
let values = [true, false, 'hello', '', NaN, -5, 1, 0, undefined, null];
singleNegation(values); // true, false, true, false,  true,  true,  true,  true, false, false,  true
doubleNegation(values); // false, true, false, true, false, false, false, false, true, true, false
```
