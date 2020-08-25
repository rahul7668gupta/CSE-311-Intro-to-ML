## Array

#### Example 1: Code for initialising numpy array


```python
import numpy as np
a = np.array([0,1,2])
type(a)
```




    numpy.ndarray




```python
a.shape
```




    (3,)




```python
a[0]
```




    0




```python
a[1]
```




    1




```python
a[2]
```




    2




```python
a[0] = 5
a
```




    array([5, 1, 2])




```python
b = np.array([[0,1,2], [3,4,5]])
b.shape
```




    (2, 3)




```python
b
```




    array([[0, 1, 2],
           [3, 4, 5]])




```python
print(b[0,0], b[0,1], b[1,0])
```

    0 1 3
    

#### Example 2: Creating Numpy Array


```python
a = np.zeros((3,3))
a
```




    array([[0., 0., 0.],
           [0., 0., 0.],
           [0., 0., 0.]])




```python
b = np.ones((2,2))
b
```




    array([[1., 1.],
           [1., 1.]])




```python
c = np.full((3,3), 7)
c
```




    array([[7, 7, 7],
           [7, 7, 7],
           [7, 7, 7]])




```python
d = np.random.random((3,3))
d
```




    array([[0.40951441, 0.83507637, 0.27413   ],
           [0.01683393, 0.15580447, 0.73449536],
           [0.63614583, 0.10105277, 0.39677683]])




```python
e = np.eye(3)
e
```




    array([[1., 0., 0.],
           [0., 1., 0.],
           [0., 0., 1.]])




```python
x = [1,2,3,4,4]
print(x)
f = np.array(x)
f
```

    [1, 2, 3, 4, 4]
    




    array([1, 2, 3, 4, 4])




```python
np.arange(20)
```




    array([ 0,  1,  2,  3,  4,  5,  6,  7,  8,  9, 10, 11, 12, 13, 14, 15, 16,
           17, 18, 19])




```python
np.arange(1,8, dtype = np.float)
```




    array([1., 2., 3., 4., 5., 6., 7.])




```python
np.linspace(2,4,10)
```




    array([2.        , 2.22222222, 2.44444444, 2.66666667, 2.88888889,
           3.11111111, 3.33333333, 3.55555556, 3.77777778, 4.        ])



## Data Types

#### Example 3: Numpy data types


```python
x = np.array([0,1])
```


```python
y = np.array([2.0, 3.0])
```


```python
z = np.array([5,6], dtype=np.int64)
```


```python
print(x.dtype, y.dtype, z.dtype)
```

    int32 float64 int64
    

## Array indexing

#### Example 4: indexing in numpy


```python
arr = np.array([[-1,2,0,4], [4, -0.5, 6, 0], [2.6, 0, 7, 8], [3, -7, 4, 2.0]])
```


```python
arr[:2, ::]
```




    array([[-1. ,  2. ,  0. ,  4. ],
           [ 4. , -0.5,  6. ,  0. ]])




```python
arr[[0,1,2,3], [3,2,1,0]]
```




    array([4., 6., 0., 3.])




```python
cond = arr > 0
arr[cond]
```




    array([2. , 4. , 4. , 6. , 2.6, 7. , 8. , 3. , 4. , 2. ])



## Basic Array Operations

#### Example 5


```python
a = np.array([1,2,5,3])
a+1
```




    array([2, 3, 6, 4])




```python
a-3
```




    array([-2, -1,  2,  0])




```python
a*10
```




    array([10, 20, 50, 30])




```python
a**2
```




    array([ 1,  4, 25,  9], dtype=int32)




```python
a
```




    array([1, 2, 5, 3])




```python
a*=2
a
```




    array([ 4,  8, 20, 12])




```python
a = np.array([[1,2,3],[4,5,6],[7,8,9]])
a
```




    array([[1, 2, 3],
           [4, 5, 6],
           [7, 8, 9]])




```python
a.T
```




    array([[1, 4, 7],
           [2, 5, 8],
           [3, 6, 9]])




```python
a
```




    array([[1, 2, 3],
           [4, 5, 6],
           [7, 8, 9]])



## Example 6: Unary Operators


```python
a = np.array([[1,5,6], [4,7,2], [3,1,9]])
```


```python
a.max()
```




    9




```python
a.max(axis = 1)
```




    array([6, 7, 9])




```python
a.min()
```




    1




```python
a.min(axis = 0)
```




    array([1, 1, 2])




```python
a.sum()
```




    38




```python
# cumulative sum
```


```python
a.cumsum(axis = 1)
```




    array([[ 1,  6, 12],
           [ 4, 11, 13],
           [ 3,  4, 13]], dtype=int32)



#### Example 7: Binary Operators


```python
a = np.array([[1,2],[3,4]])
b = np.array([[4,3],[2,1]])
```


```python
# elementwise addition
```


```python
a+b
```




    array([[5, 5],
           [5, 5]])




```python
# elementwise multiplication
```


```python
a*b
```




    array([[4, 6],
           [6, 4]])




```python
# matrix multiplication
```


```python
a.dot(b)
```




    array([[ 8,  5],
           [20, 13]])



#### Example 8: Universal Functions


```python
a = np.array([0, np.pi/2, np.pi])
np.sin(a)
```




    array([0.0000000e+00, 1.0000000e+00, 1.2246468e-16])




```python
Exponent Function: e^x
```


```python
np.exp(a)
```




    array([ 1.        ,  4.81047738, 23.14069263])




```python
np.sqrt(a)
```




    array([0.        , 1.25331414, 1.77245385])



## Matrix Inverse

#### Example 9


```python
a = np.array([[1,5,6], [4,7,2], [3,1,9]])
```


```python
inverse = np.linalg.inv(a)
inverse
```




    array([[-0.31937173,  0.20418848,  0.16753927],
           [ 0.15706806,  0.04712042, -0.11518325],
           [ 0.08900524, -0.07329843,  0.06806283]])



# End
