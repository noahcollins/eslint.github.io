---
title: ESLint
layout: doc
---
# Disallow Variables Deletion

This rule prevents the use of `delete` operator on variables:

```javascript
var x;
delete x;
```

The delete operator will only delete the properties of objects. It cannot "delete" variables or anything else. Using them on variables might lead to unexpected behavior.

## Further Reading

* [Only properties should be deleted](http://jslinterrors.com/only-properties-should-be-deleted/)