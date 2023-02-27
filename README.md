# Patikadev-PythonLists

***

## input: [[1,'a',['cat'],2],[[[3]],'dog'],4,5]
## output: [1,'a','cat',2,3,'dog',4,5]

```python
list1 = [[1,'a',['cat'],2],[[[3]],'dog'],4,5]
list2 = []
def flatten(l):
    flattening = [flatten(sublist) if type(sublist) == list else list2.append(sublist) for sublist in l]
flatten(list1)
print(list2) # [1,'a','cat',2,3,'dog',4,5]
```

***

## input: [[1, 2], [3, 4], [5, 6, 7]]
## output: [[[7, 6, 5], [4, 3], [2, 1]]

```python
list1 = [[1, 2], [3, 4], [5, 6, 7]]
def reverse_list(l):
    l.reverse()
    reverse = [reverse_list(sublist) for sublist in l if type(sublist) == list]
reverse_list(list1)
print(list1) # [[[7, 6, 5], [4, 3], [2, 1]]
```
