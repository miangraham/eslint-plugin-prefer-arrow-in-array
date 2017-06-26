# eslint-plugin-prefer-arrow-in-array

A plugin+rule to suggest arrow functions over function expressions as array elements.

Made for people still using async.waterfall([]) for some reason. (Don't do this. Use async/await instead.)

Quick hacky fork of prefer-arrow-callback from eslint core rules. Original author: Toru Nagashima. Original LICENSE preserved.

## Usage
```
---
plugins:
    - prefer-arrow-in-array
rules:
    - prefer-arrow-in-array/prefer-arrow-in-array
```
