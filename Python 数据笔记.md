## Python 数据笔记

### Numpy

```python
arr = np.array([[2,3,1], [6,4,5], [7,8,9]])
type(arr), arr.dtype
```

`type`返回Python类型，`.dtype`返回元素的数据类型。

```python
arr[2][1], arr[2,1]
```

`arr[2]` 会生成一个新的数组。 

```python
np.concatenate(arr1, arr2, axis=0)
```

级联函数中`0,1`代表**靠**行、列联接，不是**按**行、列执行；其他函数是**按**行、列执行。

```python
arr1 = np.append(np.arange(0,11), np.repeat(np.nan, 5))
np.sum(arr1), np.nansum(arr1), np.percentile(arr1, 40), np.nanpercentile(arr1, 40)
```

`np.nansum`会忽略缺失，`np.sum`不会而是返回`np.nan`。 

```python
arr = np.random.randint(0, 10, size=(3,4))
for i in arr:
    print(i)

for arr_i in arr:
    for j in arr_i:
        print(j)

for i in arr.flat:
    print(i)
```

第一个`arr[i]`得到第`i`个一维数组。`arr.flat`会进行拷贝和扁平化，最后得到第`i`个元素。


