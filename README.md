# eslint-plugin-prefer-arrow-in-array

An ESLint plugin+rule to suggest arrow functions over function expressions as array elements.

Made for a project that's still using async.waterfall. (Don't do this. Use async/await instead.)

Quick hacky fork of [prefer-arrow-callback](http://eslint.org/docs/rules/prefer-arrow-callback) from the ESLint core rules.

Original author: [Toru Nagashima](https://github.com/mysticatea). Original [LICENSE](./LICENSE) (MIT) preserved.

## Configuration
.eslintrc additions:
```yaml
---
plugins:
    - prefer-arrow-in-array
rules:
    - prefer-arrow-in-array/prefer-arrow-in-array: error
```

## Disallowed
```js
async.waterfall([
  function (next) {
    const foo = 'bar';
    return next(null, foo);
  },
  // ...
],
  // ...
);
```

## Allowed (autofixed)
```js
async.waterfall([
  next => {
    const foo = 'bar';
    return next(null, foo);
  },
  // ...
],
  // ...
);
```
