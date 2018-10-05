# Advanced-JavaScript
Notes taken while reading articles and books like "JavaScript Allongé"

### Comma 
This operator takes two arguments, evaluates them both, and itself evaluates to the value of the right-hand argument. In other words:
```
(1 + 1, 2 + 2)
  //=> 4
```

So, this is a valid function:

() => {}

### Undefined
In JavaScript, the absence of a value is written undefined, and it means there is no value. It has its own type of value, and it acts like a value type:

```
undefined
  //=> undefined
```
In JavaScript, every undefined is identical to every other undefined.
When we deliberately want an undefined value use **void(expr)**.

### Expressions, statements and blocks
A block is a (possibly empty) list of JavaScript statements separated by semicolons:

```{ statement1; statement2; statement3; ... ; statementn }```

An expression is a kind of JavaScript statement. Other kinds of statements are function declarations, for loops, if statements, and so forth.
Statements belong inside blocks and only inside blocks. Some languages simplify this by making everything an expression, but JavaScript maintains this distinction.
```
(() => return 0)()
 //=> ERROR
```

The **return** keyword creates a return statement that immediately terminates the function application and returns the result of evaluating its expression. For example:
```
(() => {
    1 + 1;
    return 2 + 2
  })()
  //=> 4
```

If an expression that evaluates to a function is an expression, and if a return statement can have any expression on its right side, then
**we can put an expression that evaluates to a function on the right side of a function expression**

```
() => () => true
(() => () => true)()()
  //=> true
```

Expressions consist either of representations of values (like 3.14159265, true, and undefined), operators that combine 
expressions (like 3 + 2), some special forms like [1, 2, 3] for creating arrays out of expressions, 
or function (arguments) {body-statements} for creating functions.

### Variables and bindings

Every time a function is invoked (“invoked” means “applied to zero or more arguments”), a new environment is created. An environment is a (possibly empty) dictionary that maps variables to values by name.

