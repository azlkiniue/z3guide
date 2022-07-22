
# This file is to contain more tests


including samples for which there are python variants for side-to-side learning


```z3-js
const x = Z3.Int.const('x');

const solver = new Z3.Solver();
solver.add(Z3.And(x.ge(10), x.le(9)));
await solver.check();
```



Porting guide:

```z3-python
x = Int('x')
y = Int('y')
solve(x > 2, y < 10, x + 2*y == 7)
```

```z3-js
const x = Z3.Int.const('x')
const y = Z3.Int.const('y')
Z3.solve(x.gt(2), y.lt(10), x.add(y.mul(2)).eq(7))
```

```z3-python
x = Int('x')
y = Int('y')
print (simplify(x + y + 2*x + 3))
print (simplify(x < y + x + 2))
print (simplify(And(x + 1 >= 3, x**2 + x**2 + y**2 + 2 >= 5)))
```

``z3-js
x = Z3.Int('x')
y = Z3.Int('y')
Z3.simplify(x.add(y).add(x.mul(2)).add(3))
```



