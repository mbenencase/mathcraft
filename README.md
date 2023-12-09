# PyLab

Python Laboratory. Our purpose is to provide a simple toolbox, with a wide-range of features, that allows academics, STEM students and entushiasts on building their applications simple as possible.

## How to Install

We've uplaoded to PyPi organization, so you can install it as follows:

```
pip install mathcraft
```

## Dependencies

- Python 3.9 or above.

`MathCraft` is build using NumPy. We include also `beartype` dependency because we want to guarantee code quality and coverage across the time.

## How to Use

### Vector Class

The Vector class provides a NumPy array-like initialization, however it enforces the shape (N, 1) of the vector.

```
from mathcraft import Vector

x1 = Vector([1, 2, 3])
x2 = Vector(np.array([3, 4, 5, 1, 3, 5]))
```

We included a method to make simpler the computation of the vector norm.

```
v = Vector([1, 2, 3, 4, 5, 6])
norm = v.norm()

print(norm)
```

You can also return a normalized vector if you already have created one:

```
v = Vector([1, 2, 3, 4, 5, 6])
w = Vector([1, 2, 3, 4, 5, 6])

dotProd_vw = v.normalized().T @ w.normalized()
print(dotProd_vw)
```

### Matrix Class

The same for our Matrix class:

```
from mathcraft import Matrix

A = Matrix([[2, 3], [4, 5]])
B = Matrix(np.array([[2, 3], [4, 5]]))
```

We included methods to make the computation of determinant and inverse/pseudo-inverse easier:

```
A = Matrix([[2, 3], [4, 5]])
print(A.inv())
print(A.det())
print(A.pinv())
print(A.T)
```

## Contribute

If you want to contribute to the project, check the [TODO](TODO.md) file. Create your code and do a PR.