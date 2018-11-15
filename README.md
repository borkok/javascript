[https://stackoverflow.com/questions/523643/difference-between-and-in-javascript](https://stackoverflow.com/questions/523643/difference-between-and-in-javascript)

JavaScript has both **strict and type-converting equality comparison**. For`strict`equality the objects being compared must have the same type and:

* Two strings are strictly equal when they have the same sequence of characters, same length, and same characters in corresponding positions.
* Two numbers are strictly equal when they are numerically equal \(have the same number value\).
  `NaN`is not equal to anything, including`NaN`. Positive and negative zeros are equal to one another.
* Two Boolean operands are strictly equal if both are true or both are false.
* Two objects are strictly equal if they refer to the same`Object`.
* `Null`and`Undefined`types are`==`\(but not`===`\). \[I.e. \(`Null==Undefined`\) is`true`but \(`Null===Undefined`\) is`false`

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

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison\_Operators

JavaScript has both strict and type–converting comparisons. A **strict comparison \(e.g.,`===, !==`\) **is only true if the operands are of the same type and the contents match. The more commonly-used** abstract comparison \(e.g.`==, !=`\) **converts the operands to the same type before making the comparison. For** relational abstract comparisons \(e.g.,`<=`\)**, the operands are first converted to primitives, then to the same type, before comparison.

Strings are compared based on standard lexicographical ordering, using Unicode values.

If **both operands are objects**, then JavaScript compares internal references which are equal when operands refer to the same object in memory.

```
var object1 = {'key': 'value'}, object2 = {'key': 'value'}; 
object1 == object2 //false
```

```
1 !=   2     // true
1 !=  '1'    // false
1 !=  "1"    // false
1 !=  true   // false
0 !=  false  // false

1    ==  1         // true
'1'  ==  1         // true
1    == '1'        // true
0    == false      // true

3 === 3   // true
3 === '3' // false
var object1 = {'key': 'value'}, object2 = {'key': 'value'};
object1 === object2 //false

3 !== '3' // true
4 !== 3   // true
```



