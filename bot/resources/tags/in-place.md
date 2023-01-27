**Out of Place** and **In Place**

In programming, there are two types of operations: "out of place" and "in place". An "out of place" operation creates a new object, leaving the original object unchanged. An "in place" operation modifies the original object, without creating a new one. These operations return None explicitly.

A common example of these different concepts is seen in the use of the methods `list.sort()` and `sorted(...)`. Using `list.sort()` and attempting to access an element of the list after calling `sort()` will result in an error. 

```py
a_list = [3, 1, 2]
a_new_list = a_list.sort() # This will be None
print(a_new_list[1]) # This will error because it is NoneType and not a list

a_list = [3, 1, 2]
sorted(a_list)
print(a_list[0]) # You may expect 1, but it will print 3
```

To avoid these errors and unexpected results, it is required to assign the result of `sorted(...)` to a new variable and use `list.sort()` method in the original list. This way, the original list will be sorted and the new list will be created with the sorted elements.