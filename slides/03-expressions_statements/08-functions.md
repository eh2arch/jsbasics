title: Function definitions
---
There are two syntactic constructs to create functions: function **declaration**
and function **expressions**.

**Function declarations** start with the `function` keyword followed by a
**name**, the parameter list and the function body:

```
function foo(a, b, c) {
  // do something
}
```

**Function expressions** have the same structure, but their name is optional:

```
var foo = function(a, b, c) {
  // do something
};
```
<div class="alert alert-info">
<strong>Note:</strong> Since functions are objects, they can be treated like any
other value. They can be assigned to variables, passed to other functions and
returned from functions. The code above is just an assignment expression with a
function as value.
</div>

All function objects created either way behave exactly the same. Whether the
parser treats a function definition as declaration or expression depends on
where the definition is placed. If it is in a expression context, it as
interpreted as expression, otherwise as declaration. That's why

```
function () { }
```

generates an error (function declaration without name), but

```
(function () { })
```

does not, because the grouping operator (`(...)`) can only contain expressions.