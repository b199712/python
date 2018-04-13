# Python基本語法

## print
```python
print 'Hello world!'  # (X)
```
```python
print('Hello world!') # (O)
```

可以在一開始加上
```python
from __future__ import print_function
```
就會檢查`print`

## variable
```python
var1 = 123
type(var1) # int
```
```python
var2 = '123'
type(var2) # string
```
```python
var3 = 12.3
type(var3) # float
```

## String with format
```python
item = 'abc'
result = 'FAIL'
print('The test item ' + item + ' is ' + result + '.')      # (X)
print('The test item {} is {}.'.format(item, result))       # (O)
print('The test item {i} is {r}.'.format(r=result, i=item)) # (O)
```

## User input
```python
num = input('Input a number:')
print(num)
```

## Indentation
python判斷區塊的方法是依照縮排來決定

Tab     (X)

4 space (O)

## if elif else
```python
var = None
if var:
    print('is True')
elif not var:
    print('is False')
else:
    print('Unknown')
```

## for
```python
for i in range(0, 5):
    print(i)

# 0
# 1
# 2
# 3
# 4
```

## list
```python
list_test = ['a', 'b', 'c', 'd', 'e']
len(list_test) # 5
list_test.index('c') # 3
list_test.append('12345') # ['a', 'b', 'c', 'd', 'e', '12345']
list_test.extend('12345') # ['a', 'b', 'c', 'd', 'e', '1', '2', '3', '4', '5']
list.insert(0, 'f') # ['f', 'a', 'b', 'c', 'd', 'e']
```

## tuple (cannot be changed)
```python
tuple_test = ('a', 'b', 'c', 'd', 'e')
```

## Dictionary
```python
dict = {
    'Name': 'ALOHA',
    'Man': True,
    'Age': 50
}
dict['height'] = 200.3
```

## for in list, tuple and dictonary
```python
# list, tuple
for index, value in enumerate(list_test):
    print(index, value)

# (0, 'a')
# (1, 'b')
# (2, 'c')
# (3, 'd')
# (4, 'e')

# dictonary
for key, value in dict.iteritems():
    print(key, value)

# ('Name', 'ALOHA')
# ('Man', True)
# ('Age', 50)
```

## import
```python
import os
from datetime import datetime
from import_file import common as com
```

## function
```python
def func1():
    print('This is func')

func1() # This is func

def func2(var1, var2=123):
    print('var1: {}, var2: {}'.format(var1, var2))

func2('abc') # var1:ttt, var2: 123
func2('ttt', 456) # var1:ttt, var2: 456

def func3(*args):
    '''
    傳入的變數會以Tuple的型態顯示
    '''
    print(args)

func3(1, 2, 3, 4, 5) # (1, 2, 3, 4, 5)

def func4(**kwargs):
    '''
    傳入的變數會以Dictionary型態顯示
    '''
    print(kwargs)

func4(a=1, b=2, c=3) # {'a': 1, 'c': 3, 'b': 2}
```
如果有中文字在檔案中請再開頭加上
```python
# -*- coding: utf-8 -*-
```

## Class
```python
class Test():
    '''
    一般的function第一個變數都會是self
    如果function或者variable前面為__或者_開頭則代表限定此class內使用
    '''
    def __init__(self, var1):
        '''
        剛建立時會呼叫到的function
        '''
        self.var1 = var1

    def print_var(self):
        print(self.var1)

ttt = Test('abc')
ttt.print_var()
```

## is and ==
http://cm8947.blogspot.tw/2015/05/python-is.html
