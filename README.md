https://stackoverflow.com/questions/523643/difference-between-and-in-javascript

JavaScript has both **strict and type-converting equality comparison**. For`strict`equality the objects being compared must have the same type and:

* Two strings are strictly equal when they have the same sequence of characters, same length, and same characters in corresponding positions.
* Two numbers are strictly equal when they are numerically equal \(have the same number value\).
  `NaN`
  is not equal to anything, including
  `NaN`
  . Positive and negative zeros are equal to one another.
* Two Boolean operands are strictly equal if both are true or both are false.
* Two objects are strictly equal if they refer to the same
  `Object`
  .
* `Null`
  and
  `Undefined`
  types are
  `==`
  \(but not
  `===`
  \). \[I.e. \(
  `Null==Undefined`
  \) is
  `true`
  but \(
  `Null===Undefined`
  \) is
  `false`
  \]

```
The 3 equal signs mean "equality without type coercion". Using the triple equals, the values must be equal in type as well.

0 == false   // true
0 === false  // false, because they are of a different type
1 == "1"     // true, automatic type conversion for value only
1 === "1"    // false, because they are of a different type
null == undefined // true
null === undefined // false
'0' == false // true
'0' === false // false
```



