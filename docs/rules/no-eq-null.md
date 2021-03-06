---
title: ESLint
layout: doc
---
# Disallow Null Comparisons

Comparing to `null` without a type-checking operator (`==` or `!=`), can have unintended results as the comparison will evaluate to true when comparing to not just a `null`, but also an `undefined` value.

```js
if (foo == null) {
  bar();
}
```

## Rule Details

The `no-eq-null` rule aims reduce potential bug and unwanted behavior by ensuring that comparisons to `null` only match `null`, and not also `undefined`. As such it will flag comparisons to null when using `==` and `!=`.

The following patterns are considered warnings:

```js
if (foo == null) {
  bar();
}

while (qux != null) {
  baz();
}
```

The following patterns are considered okay:

```js
if (foo === null) {
  bar();
}

while (qux !== null) {
  baz();
}
```
