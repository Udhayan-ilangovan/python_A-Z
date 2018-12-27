
# PYTHON 3 A - Z

## Let's start with Hello World


```python
print("Hello world")
```

    Hello world


Python Data Types

NAME           => DESCRIPTION                                               => TYPE

Integer        => whole numbers (1, 45, 800)                                => Int

Floating Point => Decimals (1.0, 45.8, 800.008)                             => float

String         => Sequence of Characters inside "" or ''                    => str

List           => ordered sequence of object ['hello',"123","world,100.6"]  => list

Dictionary     => key and value pair => {"hi":"hello","Key":"Value"}        => dict

Tuples         => Imutable sequence of object ('hello',"123","world,100.6") => tup

Sets           => unordered collection of unique object {"a","b"}           => set

Boolean        => True or false binary output                               => bool


Arithmetic operation 

1. Addition 


```python
10+5
```




    15



2. Subtraction 


```python
10-5
```




    5



3. Multiplication 


```python
10*5
```




    50



4. Division 


```python
10/5
```




    2.0



5. Mod
    It gives the reminder as output


```python
10%5
```




    0



6. Exponents


```python
10**2
```




    100



## Python operator precedence are listed below. 
### It is in descending order. Higher to Lower

#### NO. OPERATORS => MEANING

1. () => Parentheses

2. **	Exponent

3. +x, -x, ~x => Unary plus, Unary minus, Bitwise NOT

4. *, /, //, % => Multiplication, Division, Floor division, Modulus

5. +, - => Addition, Subtraction

6. <<, >> => Bitwise shift operators

7. & => Bitwise AND

8. ^ => Bitwise XOR

9. | => Bitwise OR

10. ==, !=, >, >=, <, <=, is, is not, in, not in => Comparisions, Identity, Membership operators

11. not => Logical NOT

12. and => Logical AND

13. or => Logical OR



```python
1+2-3*4/5

```




    0.6000000000000001




```python
1+2-3*4/5 == (1+2-3*4/5)
```




    True



## VARIABLE

Variables are reference to datatypes 

which are reserved memory locations to store values.

Lowercase is preferable.

Avoid predifiend keyword

Variables can be used as it is not static


```python
# Assigning the values
a = 1
b = 2
c = a + b
# Printing the c
print (c)
# Adding the c by itself
c = c + c
print(c)
# To know the Data type
c = 1+2-3*4/5
print(c)
type(c)
```

    3
    6
    0.6000000000000001





    float



## STRING

Sequence of characters 

Inside "" or ''

String in python are Immutable

Uses Indexing

In python index starts at 0

Python also has reverse indexing and it starts at -1

Slicing is available in python string 

    It has
    
        starting index 
        
        ending index
            
            Not included
        
        Skiping or jump
        
        [start:stop:skip]
    


```python
#assigning the string to variable
a = "Hello world"
print(a)
# Grabing the first index
b = a[0]
# Grabing the last index
c = a[-1]
# Grabing the required sequence of index 
d = a[0:5]
# Grabing the required sequence of index with step size of skipping by 2
e = a[0:5:2]
# Grabing the required sequence from the index 4
f = a[4:]
# Grabing the required sequence upto the index 4
g = a[:4]
# Grabing the required sequence from the index -3
h = a[-3:]
# Grabing the required sequence of index with skipping by 3
i = a[::3]

# GReversing the string 
j = a[::-1]
print(c)
print("******************************")
print(d)
print("******************************")
print(e)
print("******************************")
print(f)
print("******************************")
print(g)
print("******************************")
print(h)
print("******************************")
print(i)
print("******************************")
print(j)
print("******************************")
#printing the length of the string
print(len(a))
print("******************************")
print(len(c))
print("******************************")
print(len(d))
print("******************************")
k = len(e)
print("******************************")
print(k)
print("******************************")
#concatenation of string && it should in string datatype
l = d + a[-5:]
print(l)
print("******************************")
# Adding tab space and multipling the string 
m = (l+"\t")*3
print(m)
print("******************************")
# Adding new line space
n = d+"\n"+ a[-5:]
print(n)
print("******************************")
# using Default function
o = a.upper()
print(o)
print("******************************")
p = o.isupper()
print(p)
print("******************************")
#splitting and adding to list && default white space
q = o.split()
print(q)
print(type(q))
print("******************************")
#splitting using the chsractor
r = o.split("L")
print(r)
print("******************************")

#Join using the string
st = "hello world, how are you"
st_sp = st.split()
print(f"\nThis is printed after Splitting => {st_sp}\n")
st_sp_j_s = " ".join(st_sp)
st_sp_j_p = "|".join(st_sp)
print(f"\nThis is printed after joining using ' ' => {st_sp_j_s}\nThis is printed after joining using '|' => {st_sp_j_p}\n")
```

    Hello world
    d
    ******************************
    Hello
    ******************************
    Hlo
    ******************************
    o world
    ******************************
    Hell
    ******************************
    rld
    ******************************
    Hlwl
    ******************************
    dlrow olleH
    ******************************
    11
    ******************************
    1
    ******************************
    5
    ******************************
    ******************************
    3
    ******************************
    Helloworld
    ******************************
    Helloworld	Helloworld	Helloworld	
    ******************************
    Hello
    world
    ******************************
    HELLO WORLD
    ******************************
    True
    ******************************
    ['HELLO', 'WORLD']
    <class 'list'>
    ******************************
    ['HE', '', 'O WOR', 'D']
    ******************************
    
    This is printed after Splitting => ['hello', 'world,', 'how', 'are', 'you']
    
    
    This is printed after joining using ' ' => hello world, how are you
    This is printed after joining using '|' => hello|world,|how|are|you
    


## STRING FORMAT METHOD

printing during runtime using the metho .format() 

the values inside the format is list and separated by 

for example .format("hi","hello") in this hi is at index 0 and hello is at index 1

if {} inside the string is not equal to the contrnt inside format it throws error

    Example ERROR : print("This {0} is printed using {2}.format("hello"))
    
    To avoid this use indexing
    
Values can be repeated using indexing repeatedly 


```python
print("This {0} is printed using {2} {1} and it can also print numbers {3}{3},{3}".format("hello","Method","format",5,"Extra values 'indexing avoid error'"))
print("******************************")
s = "Formated output  can be assigned to variables *** {0} *** {0}".format("'indexing avoid error'")
print(s)
print("******************************")
# values inside format this to variable
t = "Format values can be assigned to variables *** {vari} *** {vari}".format(vari = "assigined to variable")
print(t)
print("******************************")

# Formating the float using format
# 4f and 6f is the values included after . that is decimal 
# 5 and 8 are the width values
a = 0.45374684
b = "Formating the float value {v:5.4f}".format(v = a)
print(b)
print("******************************")
c = 1234.45374684
d = "Formating the float value {v:8.6f}".format(v = c)
print(d)


```

    This hello is printed using format Method and it can also print numbers 55,5
    ******************************
    Formated output  can be assigned to variables *** 'indexing avoid error' *** 'indexing avoid error'
    ******************************
    Format values can be assigned to variables *** assigined to variable *** assigined to variable
    ******************************
    Formating the float value 0.4537
    ******************************
    Formating the float value 1234.453747


## Formated String or fstring

similar to fstring
In this values can be included directly


```python
num = 10
string = "hello this is string"
print(f"This is printed using fstring method : '{string} ' \n And it can also print numbers and repeatedly : {num}{num},{num}")
print("******************************")
a = f"This values are assigned to variable using fstring method : '{string} ' \nAnd it can also print numbers and repeatedly : {num}{num},{num}"
print(a)
print("******************************")

```

    This is printed using fstring method : 'hello this is string ' 
     And it can also print numbers and repeatedly : 1010,10
    ******************************
    This values are assigned to variable using fstring method : 'hello this is string ' 
    And it can also print numbers and repeatedly : 1010,10
    ******************************


## LIST
1. List are ordered Sequence that holds varieties of objects seperated by commas
2. List can contain any kind of objects
3. It starts with [ and ends with ] and seperated by , like [1,"a",2,4].
4. List supports indexing, slicing and it also has useful pre-defiend methods.


```python
int_list = [1,2,3,4,5]
str_list = ["hi","Hello","World"]
mixed_list = ["Hello",2,4.04,"bye"]
print(f" int_list {int_list}\n str_list {str_list} \n mixed_list {mixed_list}")
```

     int_list [1, 2, 3, 4, 5]
     str_list ['hi', 'Hello', 'World'] 
     mixed_list ['Hello', 2, 4.04, 'bye']



```python
# retriving by index
li_in = str_list[2]
# slicing 
l1 = int_list[2:]
l2 = int_list[-2:]
l3 = int_list[-4:3]
l4 = int_list[2:-1]
print(f" li_in {li_in} \n ****\n l1 {l1}\n l2 {l2} \n l3 {l3} \n l4 {l4}")
```

     li_in World 
     ****
     l1 [3, 4, 5]
     l2 [4, 5] 
     l3 [2, 3] 
     l4 [3, 4]



```python
# Concatenazione of list
con_list = mixed_list + int_list
print(f" cin_list {con_list}")
# list are mutable 
con_list[0] = "updated value"
print(f" After updating cin_list {con_list}")
# to know the length 
print(f"Length {len(con_list)}")
```

     cin_list ['Hello', 2, 4.04, 'bye', 1, 2, 3, 4, 5]
     After updating cin_list ['updated value', 2, 4.04, 'bye', 1, 2, 3, 4, 5]
    Length 9



```python
# To Adding new values to list
int_list.append(1)
print(f" After adding {int_list}")
# To Delete a value from list 
int_list.pop()
print(f" After removing {int_list}")
deleted_value = int_list.pop(1)
print(f" After removing by index {int_list}")
print(f" Removed value {deleted_value}")

```

     After adding [1, 2, 3, 4, 5, 1]
     After removing [1, 2, 3, 4, 5]
     After removing by index [1, 3, 4, 5]
     Removed value 2



```python
# sorting a list
# should habe same datatype
# int and float
int_so_list = [1,58,3,5,2.9,959,2,0]
int_so_list.sort()
print(f" Sorted List {int_so_list}")
# string and character
str_so_list = ["hello","world","bye","a",'c']
str_so_list.sort()
print(f" Sorted List {str_so_list}")
# Desecing of sorted list a list
con_list.reverse()
print(f" Sorted List {con_list}")

```

     Sorted List [0, 1, 2, 2.9, 3, 5, 58, 959]
     Sorted List ['a', 'bye', 'c', 'hello', 'world']
     Sorted List ['updated value', 2, 4.04, 'bye', 1, 2, 3, 4, 5]


## APPENDING LIST VS EXTENDING LIST
1. Append add the value as it is to the list
2. Extend add the value as single element in the list


```python
# List extend()
fir_list = [1,2,5,6]
sec_list = [3,4,5,6,7,8]
fir_list.extend(sec_list)
print(f" Extending the List {fir_list}")
# List append()
fir_list.append(sec_list)
print(f" Appending the List {fir_list}")
```

     Extending the List [1, 2, 5, 6, 3, 4, 5, 6, 7, 8]
     Appending the List [1, 2, 5, 6, 3, 4, 5, 6, 7, 8, [3, 4, 5, 6, 7, 8]]


#### Nested List
To grab a value fom nested list, call the value by adding extra bracket


```python
nested_list = ["Master list",1,["first nested list",["Second nested list",7,[8,4,"Third nested list",9]],2]]
print(f" To print all list => {nested_list}\n")
print(f" Master List => {nested_list[0]}")
print(f" First nested list => {nested_list[2][0]}")
print(f" Second nested list => {nested_list[2][1][0]}")
print(f" Third nested list => {nested_list[2][1][2][2]}")
print(f" Third nested list full => {nested_list[2][1][2]}")
print(f" Second nested list full => {nested_list[2][1]}")
```

     To print all list => ['Master list', 1, ['first nested list', ['Second nested list', 7, [8, 4, 'Third nested list', 9]], 2]]
    
     Master List => Master list
     First nested list => first nested list
     Second nested list => Second nested list
     Third nested list => Third nested list
     Third nested list full => [8, 4, 'Third nested list', 9]
     Second nested list full => ['Second nested list', 7, [8, 4, 'Third nested list', 9]]


## DICTIONARY 
1. Dictionary uses mapping concept to store values
2. It has Key and Value
3. Keys and values can be any type.
4. Key and value are separated using : 
5. Each pairs are seperated between ,
6. All pairs are  contained inside {}
7. For example {"key":"Value","key1":"Value1","key2":"Value2"}
8. With key we can easily  call the values, so index is not needed
9. Cannot be ordered or sorted
10. It can hold list or dict


```python
str_dict = {"key":"Value","key1":"Value1","key2":"Value2"}
```


```python
str_dict["key"]
```




    'Value'




```python
veg_price_dic = {"Carrot":3.834,"beans":1.49,"onions":3.21,"tomato":4.1}
```


```python
veg_price_dic["onions"]
```




    3.21




```python
all_data_type_dic = {9:3.834,789.89:1.49,"onions":3.21,"tomato":4.1}
```


```python
a = all_data_type_dic[789.89]
b = all_data_type_dic["onions"]
c = all_data_type_dic[9]
print(f" value of a {a}, value of (b,c) {b,c}")
```

     value of a 1.49, value of (b,c) (3.21, 3.834)



```python
all_data_type_dic = {"onions":3.21,"tomato":4.1,"list":int_list,"dict":str_dict}
```


```python
d = all_data_type_dic["list"]
e = all_data_type_dic["onions"]
f = all_data_type_dic["dict"]
print(f" value of a {d}\n value of e {e}\n value of f {f}")
```

     value of a [1, 3, 4, 5]
     value of e 3.21
     value of f {'key': 'Value', 'key1': 'Value1', 'key2': 'Value2'}



```python
# To get the value of list inside the Dictionary 
ind_list = all_data_type_dic["list"][2]
# To get the value of list inside the Dictionary 
key_dict = all_data_type_dic["dict"]["key2"]
print(f" value of nested list {ind_list}\n value of nested dict {key_dict}")
```

     value of nested list 4
     value of nested dict Value2



```python
print(f" Orginal values {all_data_type_dic}")
# Using the functions of string
key_dict = all_data_type_dic["dict"]["key2"].upper()
# Using the functions of List
ind_list = all_data_type_dic["list"].pop(2)
print(f" value of nested list {ind_list}\n value of nested dict {key_dict}")
print(f" After updating values {all_data_type_dic}")

```

     Orginal values {'onions': 3.21, 'tomato': 4.1, 'list': [1, 3, 4, 5], 'dict': {'key': 'Value', 'key1': 'Value1', 'key2': 'Value2'}}
     value of nested list 4
     value of nested dict VALUE2
     After updating values {'onions': 3.21, 'tomato': 4.1, 'list': [1, 3, 5], 'dict': {'key': 'Value', 'key1': 'Value1', 'key2': 'Value2'}}



```python
# Adding value to Dictionary
str_dict = {"key":"Value","key1":"Value1","key2":"Value2"}
print(f" Before Adding values {str_dict}")
str_dict["key_added"] ="Value_added"
print(f" After Adding values {str_dict}")
```

     Before Adding values {'key': 'Value', 'key1': 'Value1', 'key2': 'Value2'}
     After Adding values {'key': 'Value', 'key1': 'Value1', 'key2': 'Value2', 'key_added': 'Value_added'}



```python
# To print Keys in dictionary 
keys_dict = str_dict.keys()
val_dict = str_dict.values()
items_dict = str_dict.items()
print(f" Keys {keys_dict}\n Value  {val_dict}\n Items  {items_dict}")
```

     Keys dict_keys(['key', 'key1', 'key2', 'key_added'])
     Value  dict_values(['Value', 'Value1', 'Value2', 'Value_added'])
     Items  dict_items([('key', 'Value'), ('key1', 'Value1'), ('key2', 'Value2'), ('key_added', 'Value_added')])


## TUPLES
1. Tuples are similar to list but Tuples are immutable 
2. Ones value is inserted it cannot be edited or updsted
3. Tuples uses Parentheses () and values are seperated by ,


```python
int_tuples = (1,2,3,4,5)
str_tuples = ("Hi","Hello","World",'hi',"Hi")
mixed_tuples = ("Hello",2,4.04,"bye")
print(f" int_tuples {int_tuples}\n str_tuples {str_tuples} \n mixed_tuples {mixed_tuples}")
```

     int_tuples (1, 2, 3, 4, 5)
     str_tuples ('Hi', 'Hello', 'World', 'hi', 'Hi') 
     mixed_tuples ('Hello', 2, 4.04, 'bye')



```python
# retriving by index
ti_in = str_tuples[2]
# slicing 
t1 = str_tuples[1:]
t2 = mixed_tuples[-2:]
t3 = int_tuples[-4:3]
t4 = int_tuples[2:-1]
print(f" ti_in {li_in} \n ****\n t1 {t1}\n t2 {t2} \n t3 {t3} \n t4 {t4}")
```

     ti_in World 
     ****
     t1 ('Hello', 'World', 'hi', 'Hi')
     t2 (4.04, 'bye') 
     t3 (2, 3) 
     t4 (3, 4)



```python
# To count number of times of occurrence of a particular element 
count_t = str_tuples.count("Hi")
# To Find the index of a particular element 
index_t = str_tuples.index("Hi") # It gives the first index
# To find the length
len_t = len(str_tuples)
print(f" count_t {count_t} \n index_t {index_t} \n len_t {len_t}")
```

     count_t 2 
     index_t 0 
     len_t 5


## SETS
1. Unordered Colections of element
2. It stores only Unique values, Duplication is not possible
3. ALL values are stored inside {} and seperated by , 


```python
int_sets = {1,2,3,4,5,5,5,5,3}
str_sets = {"Hi","Hello","World",'hi',"Hi","Hello","Hello"}
mixed_sets = {"Hello",2,4.04,"bye",4.04,4.04}
print(f" int_sets {int_sets}\n str_sets {str_sets} \n mixed_sets {mixed_sets}")
```

     int_sets {1, 2, 3, 4, 5}
     str_sets {'hi', 'Hello', 'Hi', 'World'} 
     mixed_sets {2, 'Hello', 4.04, 'bye'}



```python
# Casting tuples to set
Casted_set = set(str_tuples)
print(f" str_tuples {str_tuples}\n Casted_set {Casted_set}")
```

     str_tuples ('Hi', 'Hello', 'World', 'hi', 'Hi')
     Casted_set {'hi', 'Hello', 'Hi', 'World'}


## BOOLEANS and NONE
### Booleans
1. True or False
2. These are the results of logics 

### None
1. None are used to declar variable without values


```python
# Boolean output True And False 
out_1 = 1 < 9
out_2 = 1 > 9
print(f" out_1 {out_1}\n out_2 {out_2}")
# None Variable Declaration
empty_variable = None
type_n = type(empty_variable)
print(f" empty_variable => {empty_variable}, {type_n}")

```

     out_1 True
     out_2 False
     empty_variable => None, <class 'NoneType'>


## FILE I/O


```python
%%writefile textfile.txt
Hello these are the text which will be inside the textfile.txt 
we can give any kind Of text inside
Line 1
Line 2

#only compatible with jupiter nootbook


```

    Overwriting textfile.txt



```python
# opening or importing a file
imp_file = open("textfile.txt")
# Or one csn use full path
# imp_file = open("/Users/Machine_Learning/Python/textfile.txt")
```


```python
# to read the file
imp_file.read()
```




    'Hello these are the text which will be inside the textfile.txt \nwe can give any kind Of text inside\nLine 1\nLine 2\n\n#only compatible with jupiter nootbook\n'




```python
# To reset the cursor to read again as in python after reading the file the cursor rests at the last index of the file
bf_se_r = imp_file.read()
print(f"Reading the second time without seeking from 0 \n\t{bf_se_r}")
imp_file.seek(0)
se_0_r = imp_file.read()
print(f"Reading the value after seeked from 0 \n\t{se_0_r}")
imp_file.seek(10)
se_10_r = imp_file.read()
print(f"Reading the value after seeked from 10 \n\t{se_10_r}")

```

    Reading the second time without seeking from 0 
    	
    Reading the value after seeked from 0 
    	Hello these are the text which will be inside the textfile.txt 
    we can give any kind Of text inside
    Line 1
    Line 2
    
    #only compatible with jupiter nootbook
    
    Reading the value after seeked from 10 
    	e are the text which will be inside the textfile.txt 
    we can give any kind Of text inside
    Line 1
    Line 2
    
    #only compatible with jupiter nootbook
    



```python
# To read Line by Line
imp_file.seek(0)
# Reads all line and put into list
l_l_r = imp_file.readlines()
print(f"Reading all line and put into list  \n\t{l_l_r}\n")
imp_file.seek(0)
# Reads all line in the range and put into list
l_l_r_r = imp_file.readlines()[1:3]
print(f"Reads all line in the range and put into list \n\t{l_l_r_r}\n")
imp_file.seek(0)
```

    Reading all line and put into list  
    	['Hello these are the text which will be inside the textfile.txt \n', 'we can give any kind Of text inside\n', 'Line 1\n', 'Line 2\n', '\n', '#only compatible with jupiter nootbook\n']
    
    Reads all line in the range and put into list 
    	['we can give any kind Of text inside\n', 'Line 1\n']
    





    0




```python
# To close the file
imp_file.close()
```


```python
# To open safely a file to avoid closing problem
# As soon as the blook ends the file will close
with open("textfile.txt") as newtextfile:
    content_textfile = newtextfile.read()

print(f"Content of the text file.txt in content_textfile \n\t{content_textfile}\n")


```

    Content of the text file.txt in content_textfile 
    	Hello these are the text which will be inside the textfile.txt 
    we can give any kind Of text inside
    Line 1
    Line 2
    
    #only compatible with jupiter nootbook
    
    


### Read, Write, Append, Read & Write and Writing and reading
1. Read => r
2. Write => w
3. Append => a
4. Read & Write => r+
5. Write & Read => w+
6. Syntax open (mode = 'r')


```python
with open("textfile.txt",mode='r') as newtextfile:
    read_textfile = newtextfile.read()
print("************************************************")
print(f"Reading content_textfile \n\t{read_textfile}\n")

# Appending to the file
with open("textfile.txt",mode='a') as newtextfile:
    newtextfile.write("\nHai this is the new line using append")
    
# verifing 
with open("textfile.txt",mode='r') as newtextfile:
    verifying_textfile = newtextfile.read()
    
print("************************************************")
print(f"verifing content_textfile \n\t{verifying_textfile}\n")

# Writing to the file
with open("textfile.txt",mode='w') as newtextfile:
    newtextfile.write("\nHai this is the new line using Writing")
    
# verifing 
with open("textfile.txt",mode='r') as newtextfile:
    verifying_textfile = newtextfile.read()

print("************************************************")
print(f"verifing content_textfile \n\t{verifying_textfile}\n")


```

    ************************************************
    Reading content_textfile 
    	Hello these are the text which will be inside the textfile.txt 
    we can give any kind Of text inside
    Line 1
    Line 2
    
    #only compatible with jupiter nootbook
    
    
    ************************************************
    verifing content_textfile 
    	Hello these are the text which will be inside the textfile.txt 
    we can give any kind Of text inside
    Line 1
    Line 2
    
    #only compatible with jupiter nootbook
    
    Hai this is the new line using append
    
    ************************************************
    verifing content_textfile 
    	
    Hai this is the new line using Writing
    


## COMPARISON OPERATORS



```python
## Equal
ce = 1 == 2

## Not equal
cne = 1!= 2

## Greater
cg = 1 > 2

## Lesser
cl = 1 > 2

## Greater or equal
cge = 1 >= 2

# Lesser or equal
cle = 1 >= 2

# chain comparison && higest priorities for False
cc_1 = 1 < 2 < 3
cc_2 = 1 < 2 > 3
cc_3 = 1 < 2 >= 2

print(f"OPERATIONS => RESULT OBTAINED \nEqual => {ce} \nNot equal => {cne}\nGreater => {cg} \nLesser => {cl} \nGreater or equal => {cge} \nLesser or equal => {cle} \nchain comparison 1 => {cc_1} \nchain comparison 2 => {cc_2} \nchain comparison 3 => {cc_3}")
```

    OPERATIONS => RESULT OBTAINED 
    Equal => False 
    Not equal => True
    Greater => False 
    Lesser => False 
    Greater or equal => False 
    Lesser or equal => False 
    chain comparison 1 => True 
    chain comparison 2 => False 
    chain comparison 3 => True


## LOGICAL OPERATORS


```python
# And : All value should be true to get True
l_and = 1 < 2 and 2 > 2
# OR : Atleast one value should be true to get True
l_or = 1 < 2 or 2 > 2
# And : Gives the Opposite Boolean value
l_not = not l_and
print(f"Logical operation for AND => {l_and} \nLogical operation for OR => {l_or} \nLogical operation for NOT => {l_not}")
```

    Logical operation for AND => False 
    Logical operation for OR => True 
    Logical operation for NOT => True


## IF,ELIF and ELSE
1. IF

    if condition:
        //.....//

2. IF...ELSE

    if condition:
        //.....//
        
    else:
        //.....//
3. IF...ELIF..ELSE

   if condition:
        //.....//
   elif condition: 
        //.....//
   else condition:
        //.....//
    
4. IF...ELIF...ELIF

   if condition:
        //.....//
        
   elif condition 1: 
    .   //.....//
    .
    .
    .
    .
   elif condition n: 
        //.....//

5. IF...ELIF...ELIF...ELSE

   if condition:
        //.....//
        
   elif condition 1: 
    .   //.....//
    .
    .
    .
    .
   elif condition n: 
        //.....//
        
   else condition:
        //.....//
    
6. Colons and indent are the important sytax to be noted


```python
# if
if (1<2):
    print("1 => It is only a if condition")

# if and else
if (1>2):
    print("It is true")
else:
    print("2 => It is a if-else condition")

# if and elif
if (1>2):
    print("It is only a if condition")
elif (1==2):
     print("It is a if-elif condition")
elif (1<=2):
     print("3 => It is a if-elif condition")
else:
    print("It is a if-else condition")
    
# if elif and else
if (1>2):
    print("It is only a if condition")
elif (1==2):
     print("It is a if-elif-else condition")
elif (1>=2):
     print(" It is a if-elif-else condition")
else:
    print("5 => It is a if-elif-else condition")

```

    1 => It is only a if condition
    2 => It is a if-else condition
    3 => It is a if-elif condition
    5 => It is a if-elif-else condition


## FOR LOOP
1. Helps to create a iteration to retrive values, Printing output and much more.
2. Syntax
    
    for var in tobriterated:
        //....operations...//


```python
# printing a string 
hw_string = "Hello World"
for st in hw_string:
    print(st)
print("\n1st Block ends (String)\n")
# printing values from list
vl_list =[1,2,3,"List",6.67890,"bye"]
for vl in vl_list:
    print(vl)
print("\n2nd Block ends (List)\n")

# printing values from tuples
tp_tuple =(1,2,3,"tuples",6.67890,"bye")
for tp in tp_tuple:
    print(tp)
print("\n3rd Block ends (Tuples)\n")

# printing values from set
st_set ={1,2,3,"hello",6.67890,"bye",7,3,2,8,"hello",6.67890,"bye"}
for st in st_set:
    print(st)
print("\n4th Block ends (Set)\n")

# printing values from Dictionary 
# Note dictionaries dosent have order
dt_dictionary ={"key":"Value","key1":"Value1","key2":"Value2",3:"hello",6.67890:"bye",}
for dt in dt_dictionary:
    print(f"Printing Key => {dt}")
    print(f"Printing value => {dt_dictionary[dt]}")
print("\n5th Block ends (Dictionary)\n")
# Same Process for dictionary can be done by different procedure 
for dt_v in dt_dictionary.values():
    print(f"Printing only by using .values() function | value => {dt_v}")
print("\n5.1 Block ends (Dictionary)\n")
```

    H
    e
    l
    l
    o
     
    W
    o
    r
    l
    d
    
    1st Block ends (String)
    
    1
    2
    3
    List
    6.6789
    bye
    
    2nd Block ends (List)
    
    1
    2
    3
    tuples
    6.6789
    bye
    
    3rd Block ends (Tuples)
    
    1
    2
    3
    hello
    6.6789
    7
    8
    bye
    
    4th Block ends (Set)
    
    Printing Key => key
    Printing value => Value
    Printing Key => key1
    Printing value => Value1
    Printing Key => key2
    Printing value => Value2
    Printing Key => 3
    Printing value => hello
    Printing Key => 6.6789
    Printing value => bye
    
    5th Block ends (Dictionary)
    
    Printing only by using .values() function | value => Value
    Printing only by using .values() function | value => Value1
    Printing only by using .values() function | value => Value2
    Printing only by using .values() function | value => hello
    Printing only by using .values() function | value => bye
    
    5.1 Block ends (Dictionary)
    


## Nested Loop
1. Creating a loop inside a loop
2. Syntax 
    


```python
print("Two Nested Loop\n")
# Two nested loop
for x in range(2):
        for y in range(3):
            print(f"x => {x}, y => {y}")
print("\nThree Nested Loop\n")
# Three Nested Loop
for x in range(2):
        for y in range(2):
            for z in range(2):
                print(f"x => {x}, y => {y} ,z => {z}")
```

    Two Nested Loop
    
    x => 0, y => 0
    x => 0, y => 1
    x => 0, y => 2
    x => 1, y => 0
    x => 1, y => 1
    x => 1, y => 2
    
    Three Nested Loop
    
    x => 0, y => 0 ,z => 0
    x => 0, y => 0 ,z => 1
    x => 0, y => 1 ,z => 0
    x => 0, y => 1 ,z => 1
    x => 1, y => 0 ,z => 0
    x => 1, y => 0 ,z => 1
    x => 1, y => 1 ,z => 0
    x => 1, y => 1 ,z => 1



```python
# using conditions inside loop
# Dictionary 
dt_dictionary ={"key":"Value",6.67890:"bye","key1":"Value1",3:"hello","key2":"Value2"}
for dt in dt_dictionary:
    if type(dt) == str:
        print("\nkey type is String")
        print(f"Printing Key => {dt}")
        print(f"Printing value => {dt_dictionary[dt]}")
    elif type(dt) == int:
        print("\nkey type is Integer")
        print(f"Printing Key => {dt}")
        print(f"Printing value => {dt_dictionary[dt]}")
    elif type(dt) == float:
        print("\nkey type is Float")
        print(f"Printing Key => {dt}")
        print(f"Printing value => {dt_dictionary[dt]}")
    else:
        print("\nkey type is Unknown")
        print(f"Printing Key => {dt}")
        print(f"Printing value => {dt_dictionary[dt]}")
```

    
    key type is String
    Printing Key => key
    Printing value => Value
    
    key type is Float
    Printing Key => 6.6789
    Printing value => bye
    
    key type is String
    Printing Key => key1
    Printing value => Value1
    
    key type is Integer
    Printing Key => 3
    Printing value => hello
    
    key type is String
    Printing Key => key2
    Printing value => Value2



```python
# Tuples in list
lt_list_tuple = [(1,2),(3,4),(5,6),(7,8)]
for lt in lt_list_tuple:
    print(f"Values from first for loop {lt} \n")
    for t in lt:
        print(f"\tValues from second for loop {t} \n")

print("SECOND PROCEDURE\n")
# Same Process can be done by different procedure 
# But tuple should have same values
for (t1,t2) in lt_list_tuple:
        print(f"1st value of tuple {t1} \n")
        print(f"2nd value of tuple {t2} \n")
    
```

    Values from first for loop (1, 2) 
    
    	Values from second for loop 1 
    
    	Values from second for loop 2 
    
    Values from first for loop (3, 4) 
    
    	Values from second for loop 3 
    
    	Values from second for loop 4 
    
    Values from first for loop (5, 6) 
    
    	Values from second for loop 5 
    
    	Values from second for loop 6 
    
    Values from first for loop (7, 8) 
    
    	Values from second for loop 7 
    
    	Values from second for loop 8 
    
    SECOND PROCEDURE
    
    1st value of tuple 1 
    
    2nd value of tuple 2 
    
    1st value of tuple 3 
    
    2nd value of tuple 4 
    
    1st value of tuple 5 
    
    2nd value of tuple 6 
    
    1st value of tuple 7 
    
    2nd value of tuple 8 
    


### RANGE
1. Range is used in for loop
2. Last value in  given range is not included
    For example in range(10) it will give 0 1o 9 and it will not include 10 because it   starts from zero
3. range(Starting index, Ending index, Step size)


```python
print("Only with range\n")
# Only range
for i in range(10):
    print(i)
print("\nWith starting, ending index and stepsize\n")
# starting and ending index with stepsize
for i in range(2,10,3):
    print(i)

print("\nUsing range for index and list\n")
# range can be used for different purposes also
t_range = tuple(range(2,10,2))
print(f"\nRange => {t_range}\n")
l_range = list(range(1,20,4))
print(f"\nList => {l_range}")
```

    Only with range
    
    0
    1
    2
    3
    4
    5
    6
    7
    8
    9
    
    With starting, ending index and stepsize
    
    2
    5
    8
    
    Using range for index and list
    
    
    Range => (2, 4, 6, 8)
    
    
    List => [1, 5, 9, 13, 17]


## ENUMERATE
1. same as "in" but returns index as a Collection of tuples
2. syntax

    for i in enumerate(10):
    
        print(i)
    


```python
print("\nusing enumerate\n")
for a in enumerate ("Hello"):
    print(a)
print("\nusing enumerate and range in same loop\n")
# using enumerate and range in same loop
for a in enumerate (range(5,100,10)):
    print(a)
print("\nusing enumerate and range in same loop printing separately\n")
# using enumerate and range in same loop printing separately 
lt_list_tuple = [(1,2),(3,4),(5,6),(7,8)]
for (ind,val) in  lt_list_tuple:
        print(f"Index of Enumerated tuple {ind} \n")
        print(f"Value of Enumerated tuple {val} \n")
```

    
    using enumerate
    
    (0, 'H')
    (1, 'e')
    (2, 'l')
    (3, 'l')
    (4, 'o')
    
    using enumerate and range in same loop
    
    (0, 5)
    (1, 15)
    (2, 25)
    (3, 35)
    (4, 45)
    (5, 55)
    (6, 65)
    (7, 75)
    (8, 85)
    (9, 95)
    
    using enumerate and range in same loop printing separately
    
    Index of Enumerated tuple 1 
    
    Value of Enumerated tuple 2 
    
    Index of Enumerated tuple 3 
    
    Value of Enumerated tuple 4 
    
    Index of Enumerated tuple 5 
    
    Value of Enumerated tuple 6 
    
    Index of Enumerated tuple 7 
    
    Value of Enumerated tuple 8 
    


## ZIP
1. It will create a tuple and concat the same indexed value
2. It will zip upto the maximum of sortest index
3. Syntax

    zip(list1,list2,tuple1)


```python
list1 = ["hai_1",12,2.89403,"hello_4","how_5"]
list2 = [1,2,3,4,5,6,7,8,9]
tuple1 = (34,"tup1",3,"tup2","sin","cos","tan")

for zipped_val in zip(list2,tuple1,list1):
    print(zipped_val)
```

    (1, 34, 'hai_1')
    (2, 'tup1', 12)
    (3, 3, 2.89403)
    (4, 'tup2', 'hello_4')
    (5, 'sin', 'how_5')


## LIST COMPREHENSIONS
1. It Simplify the code and enhance the performance of the for loop
2. Operation can performed with the returend value
3. Conditions can be added at the end of the loop
4. Syntax
    
    NOTE: "-" is white-space 
    
    4.1. returend_input for grabbed_value in range_of_value conditions_if_needed
    
    4.2. Basic syntax
            
            -----x--------for-------x-------in--[1,2,3,4,5,6]--------------------
    
    4.3. With operations
            
            ----(x+2)*x----for-------x-------in--[1,2,3,4,5,6]--------------------
    
    4.4. With If condition
            
            ----(x+2)*x----for-------x-------in--[1,2,3,4,5,6]-----if (x%2)==0----
    
    4.5. If else in this order change IF..else comes next to returend_input and before for
    
            ----(x+2)*x--if (x%2)==0--else "NOT EVEN"--for-------x-------in--[1,2,3,4,5,6]
            
    4.6 Nested Loop
            
            ---x,y---for---x---in--[1,2,3,4,5,6]------for-----y-------in--[1,2,3,4,5,6]
   
5. It will work only with list but can be casted if needed



```python
# 4.2
c_2_list = [x for x in [1,2,3,4,5,6]]
print(f"syntax 4.2 => {c_2_list}\n")

# 4.3
c_3_list = [(x+2)*x for x in range(1,7)]
print(f"syntax 4.3 => {c_3_list}\n")

# 4.4
c_4_list = [(x+2)*x for x in [1,2,3,4,5,6] if (x%2)==0]
print(f"syntax 4.4 => {c_4_list}\n")

# 4.5
c_5_list = [ (x+2)*x if (x%2)==0  else "NOT EVEN" for x in [1,2,3,4,5,6] ]
print(f"Using enumerate 4.5 => {c_5_list}\n")

#4.6 
# [x,y] list in list and it can be tuple (x,y)or dictionary {x,y} in list 
c_6_list = [[x,y] for x in [1,2,3] for y in range(0,2)]
print(f"syntax 4.6 => {c_6_list}\n")

# 5
print(f"syntax 5 casted to tuple => {tuple(c_4_list)}\n")

# Using enumerate 1
c_e_list = [(x+2)*(y-2) for (x,y) in enumerate(range(1,7)) if (x%2)==0]
print(f"Using enumerate 1 => {c_e_list}\n")

# Using enumerate 2
c_e_list = [ (x,y) for (x,y) in enumerate(range(1,7)) if x > 0 and y > 0 ]
print(f"Using enumerate 2.1 => {c_e_list}\n")
c_e_list = [ (x,y) for (x,y) in enumerate(range(1,7)) if x > 0 and y < 5 ]
print(f"Using enumerate 2.1 => {c_e_list}\n")

# Creating dictionary using nested for loop
c_d_list = {"Key"+str(x):y for x in [1,2,3,4,5,6,7] for y in (1,2,3,4,5,6,7,8)}
print(f"creating dictionary using nested for loop => {c_d_list}\n\nVerifying the type for Dictionary => {type(c_d_list)}")

#Sample example to use string in list comprehensions
s_string = "Hello World this is a String"
l_letters = [w[0] for w in s_string.split()]
print(f"\nSample example to use string in list comprehensions => {l_letters}")
```

    syntax 4.2 => [1, 2, 3, 4, 5, 6]
    
    syntax 4.3 => [3, 8, 15, 24, 35, 48]
    
    syntax 4.4 => [8, 24, 48]
    
    Using enumerate 4.5 => ['NOT EVEN', 8, 'NOT EVEN', 24, 'NOT EVEN', 48]
    
    syntax 4.6 => [[1, 0], [1, 1], [2, 0], [2, 1], [3, 0], [3, 1]]
    
    syntax 5 casted to tuple => (8, 24, 48)
    
    Using enumerate 1 => [-2, 4, 18]
    
    Using enumerate 2.1 => [(1, 2), (2, 3), (3, 4), (4, 5), (5, 6)]
    
    Using enumerate 2.1 => [(1, 2), (2, 3), (3, 4)]
    
    creating dictionary using nested for loop => {'Key1': 8, 'Key2': 8, 'Key3': 8, 'Key4': 8, 'Key5': 8, 'Key6': 8, 'Key7': 8}
    
    Verifying the type for Dictionary => <class 'dict'>
    
    Sample example to use string in list comprehensions => ['H', 'W', 't', 'i', 'a', 'S']


## WHILE LOOP
1. While Loop will execute until the condition is true
2. Syntax
    
    1. while(Condition):
         //....operation....//
         
    2. while(Condition):
        //....operation....//
       else:
       //....operation....//


3. Break

    It will break the loop
    
4. Continue
    
    It will skip the current procees and proceed to next iteration
    
5. Pass

    Pass do nothing its a place holder


```python
i = 0
print("\nUsing while\n")
while(i<10):
    print(f"{i} is less than 10, so Condition is True \n")
    i +=1
print(f"{i} is not less than 10, so loop is breaked \n")

print("\nUsing while....else\n")
i = 0
while(i<10):
    print(f"{i} is less than 10, so Condition is True \n")
    i +=1
else:
    print(f"{i} is not less than 10, so loop is breaked \n")


print("\nUsing Continue, Break and Pass\n")
i = 0
while(i<10):
    i +=1
    if(i==2):
        continue
        # continue will skip the current procees and proceed to next iteration
    if (i == 8):
        print(f"{i} is equal to 10, so the Condition is True and it's breaked \n")
        break
    if(i>3 and i<6):
        pass
        print("\tPass dose nothing")
    print(f"\n{i} is less than 10, so Condition is True \n")


```

    
    Using while
    
    0 is less than 10, so Condition is True 
    
    1 is less than 10, so Condition is True 
    
    2 is less than 10, so Condition is True 
    
    3 is less than 10, so Condition is True 
    
    4 is less than 10, so Condition is True 
    
    5 is less than 10, so Condition is True 
    
    6 is less than 10, so Condition is True 
    
    7 is less than 10, so Condition is True 
    
    8 is less than 10, so Condition is True 
    
    9 is less than 10, so Condition is True 
    
    10 is not less than 10, so loop is breaked 
    
    
    Using while....else
    
    0 is less than 10, so Condition is True 
    
    1 is less than 10, so Condition is True 
    
    2 is less than 10, so Condition is True 
    
    3 is less than 10, so Condition is True 
    
    4 is less than 10, so Condition is True 
    
    5 is less than 10, so Condition is True 
    
    6 is less than 10, so Condition is True 
    
    7 is less than 10, so Condition is True 
    
    8 is less than 10, so Condition is True 
    
    9 is less than 10, so Condition is True 
    
    10 is not less than 10, so loop is breaked 
    
    
    Using Continue, Break and Pass
    
    
    1 is less than 10, so Condition is True 
    
    
    3 is less than 10, so Condition is True 
    
    	Pass dose nothing
    
    4 is less than 10, so Condition is True 
    
    	Pass dose nothing
    
    5 is less than 10, so Condition is True 
    
    
    6 is less than 10, so Condition is True 
    
    
    7 is less than 10, so Condition is True 
    
    8 is equal to 10, so the Condition is True and it's breaked 
    


## IN
1. To check the value is present in the list or tuple



```python
l_in = 100 in [1,2,3,4,5,6,7,8,9]
t_in = "cos" in (34,"tup1",3,"tup2","sin","cos","tan")

# "IN" in dictionary is only for keys
in_dictionary ={"key":"Value",6.67890:"bye","key1":"Value1",3:"hello","key2":"Value2"}
d_in = "key1" in in_dictionary
print(f"Is 100 in list => {l_in}\nIs cos in tuple => {t_in}\nIs key1 in dictionary => {d_in}\n")
```

    Is 100 in list => False
    Is cos in tuple => True
    Is key1 in dictionary => True
    


## MIN and MAX
1. Min is to find minimum value
2. Max is to find maximum value
3. It should be in same data type


```python
# List
l = [1,2,3,4,5,6,7,8,9]
l_mm = min(l)
# Tuple
t = ("tup2","sin","cos","tan")
t_mm = max(t)
# Dictionary 
d ={"key":"Value","key1":"Value1","key2":"Value2"}
d_mm = min(d)

print(f" Minimum value in list => {l_mm}\n Maximum value in list => {t_mm}\n Minimum value in Dictionary => {d_mm}\n")
```

     Minimum value in list => 1
     Maximum value in list => tup2
     Minimum value in Dictionary => key
    


## Random
1. Random is a library which has methods for numeric operation
2. some operations are 
    1.randint()
    2.Shuffle


```python
# Randint
from random import randint
rr = randint(1,1000)# from 0 to 1000
print(f"Generates a random int within given range 1 to 1000 => {rr}\n")
# Random 
# dosent take range returns a float value randomly 
from random import random
r = random()
print(f"Generates a random float value => {r}")
```

    Generates a random int within given range 1 to 1000 => 874
    
    Generates a random float value => 0.9246615258292701



```python
# Shuffle the given value and place it in the same(given) variable 
from random import shuffle
l = [1,2,3,4,5,6,7,8,9]
for i in range(1,6):
    shuffle(l)
    print(f"shuffle {i} => {l}")
```

    shuffle 1 => [8, 6, 9, 5, 7, 2, 3, 1, 4]
    shuffle 2 => [6, 3, 1, 2, 5, 7, 8, 9, 4]
    shuffle 3 => [7, 5, 4, 1, 6, 9, 8, 2, 3]
    shuffle 4 => [2, 9, 8, 6, 7, 3, 1, 4, 5]
    shuffle 5 => [7, 6, 1, 4, 8, 2, 5, 3, 9]


## INPUT
1. To get a in put value during runtime
2. It always takes the value as a string but it can be casted to int or other datatypes in future


```python
inv = input("Enter the input: ")
print(f" Given Input {inv}")
```

    Enter the input: k
     Given Input k



```python
print("hello")
```

    hello


## Method
1. Methods are bultin function

    1.Example
        1. append()
        2. type()
        3. int()
        4. randint()
        5. random()
2. Using help method we can view the information of the methods and much more.
   help(randint)


```python
# Help method
help(randint)
from random import randint
r = randint(1,1000)
print(f"Generates a random int value => {r}")
```

    Help on method randint in module random:
    
    randint(a, b) method of random.Random instance
        Return random integer in range [a, b], including both end points.
    
    Generates a random int value => 748


## Functions
1. It is ablock of code which can be reused any number of time when it's called
2. It starts with "def" and ends with():
3. Syntax

    def function_name():
        //....operations....//
        
4. Parametrised function

    4.1 It takes parameter with it 
    
    4.2 More than one is also possible
    
      def function_name(param_1):
        //....operations....// 
        
      def function_name(param_1,....,param_n):
        //....operations....// 
5. Return 

    1. It returns a value from the function
    
          def function_name():
            //....a = 1+2 ....//
            return a
            
6. Default parameter

    1. It will print the default value if value is not passed when calling the function
    
        def function_name(param_1 = "default value"):
            //....operations....// 
        
7. DocString
    1. Used to creat a note about a function 
    2. It should be written inside the function 
    3. Syntax
            def function_name():
            
            //..''' Here one can write the note '''..operations....//
        
        
    4. It can be viewed using help method
        help(function_name)
        


```python
# Function without parameter
def without_parameter():
     print("hello => Function without parameter")
        
# Function with parameter
def with_parameter(welcome,bye):
     print(f"\nFunction with parameter\n\nwelcome Message => {welcome}\nbye Message => {bye}\n ")
        
# Function with return and without parameter       
def with_return_w_o_p():
        a = 1+2 
        return a
# Function with return and with parameter
def with_return_w_p(a,b):
         print(f"Value of a is => {a}\nValue of b is => {b}\n ")
         return a**b  
# Default parameter

# DocString
def default_parm(n="NAME",a="AGE"):

        print(f"Default parameter \nName: {n}\nAge: {a}\n ")
        return "Success" 
    
    
# DocString
def doc_function(n,a):
        ''' 
          n is the Name which is a String
          a is the Age which is an Intrger
        '''
        print(f"Name: {n}\nAge: {a}\n ")
 
        
without_parameter()
print("*******************")

with_parameter("Hello world","bye have a good day\n")
print("*******************")

r_o_v = with_return_w_o_p()
print(f"Function with return and without parameter returend value => {r_o_v}\n")
print("*******************")

r_v = with_return_w_p(2,4)
print(f"Function with return and with parameter => {r_v}\n")
print("*******************")

val_d = default_parm("sam")

print("*******************")
print(f"\nDoc retrived using help method ------->\n")
doc_f = help(doc_function)
sus_message = doc_function("Jim", 22)
print(f"DocString returend value => {sus_message}")
```

    hello => Function without parameter
    *******************
    
    Function with parameter
    
    welcome Message => Hello world
    bye Message => bye have a good day
    
     
    *******************
    Function with return and without parameter returend value => 3
    
    *******************
    Value of a is => 2
    Value of b is => 4
     
    Function with return and with parameter => 16
    
    *******************
    Default parameter 
    Name: sam
    Age: AGE
     
    *******************
    
    Doc retrived using help method ------->
    
    Help on function doc_function in module __main__:
    
    doc_function(n, a)
        n is the Name which is a String
        a is the Age which is an Intrger
    
    Name: Jim
    Age: 22
     
    DocString returend value => None



```python
#Using logics
def find_char_1(c_ch="a",c_string ="string"):
    if c_ch.lower() in c_string.lower(): # to avoid case error
        return True
    else: 
        return False
rv_1 = find_char_1('z',"Hello this is a random string to check is a character is present or not")
print(f"find_char_1 => {rv_1}\n")
# same process in different Procedure 
def find_char_2(c_ch="a",c_string ="string"):
        return c_ch.lower() in c_string.lower() # to avoid case error
rv_2 = find_char_2('A',"Hello this is a random string to check is a character is present or not")
print(f"find_char_2 => {rv_2}\n")
```

    find_char_1 => False
    
    find_char_2 => True
    


## ARGS and Kwargs
1. *args => arguments

      1.1. Takes in any number of values passed while calling the parameterised function 
      
      1.2. Syntax
            def function_name(*args):
                 //....operations....//
      1.3. in this args can be replaced with any variable but using args is good practice
      
      1.4. It takes value as tuple
      
      
2. **Kargs => Keyword Arguments

      1.1. Takes in any number of values with Key passed while calling the parameterised function 
      
      1.2. Syntax
            def function_name(*kwargs):
                 //....operations....//
                 
      1.3. in this kargs can be replaced with any variable but using kargs is good practice
      
      1.4. It takes value as dictionary
      
      


```python
def sum_function(*args):
         return sum(args)
sum_val = sum_function(1,2,3,4,5,6,7,8)
print(f"Sum of given n number of input to one arg => {sum_val}")
```

    Sum of given n number of input to one arg => 36



```python
def sum_function_key(**kwargs):
        sum_v = 0
        k_n = 1
        print(f"Key_no = > key_val => current_sum")
        for _ in (kwargs):
            k_v = "key"+str(k_n)
            if  k_v in kwargs:
                sum_v = sum_v+kwargs[k_v]
                print(f"   {k_n}   = >    {kwargs[k_v]}    =>     {sum_v}")
                k_n = k_n+1
      
        print(f"\nKeys => {kwargs.keys()}\nGicve values => {kwargs.values()}\n")
        return sum_v
sum_k_val = sum_function_key(key1 =1, key2=2,key3=3, key4=4,key5=5, key6=6,key7=7,key8=8)
print(f"Sum of given n number of input to one arg => {sum_k_val}")
```

    Key_no = > key_val => current_sum
       1   = >    1    =>     1
       2   = >    2    =>     3
       3   = >    3    =>     6
       4   = >    4    =>     10
       5   = >    5    =>     15
       6   = >    6    =>     21
       7   = >    7    =>     28
       8   = >    8    =>     36
    
    Keys => dict_keys(['key1', 'key2', 'key3', 'key4', 'key5', 'key6', 'key7', 'key8'])
    Gicve values => dict_values([1, 2, 3, 4, 5, 6, 7, 8])
    
    Sum of given n number of input to one arg => 36



```python
# Adding n number of values to list
li = []
def myfunc(*args):
    print(args)
    for i in args:
        if (i%2) == 0:
            print(i)
            li.append(i)
    return li
myfunc(1,2,3,4)
```

    (1, 2, 3, 4)
    2
    4





    [2, 4]




```python
# Alternating the case of given string 
def myfunc_1(*args):
    print(args)
    v_n = 0 
    ret_val = []
    for i in range(len(args)):
        count = 1
        str_1 = ""
        for j in args[i]:
            if (count%2) == 0:
                str_1 = str_1 + j.lower() 

            else: 
                str_1 = str_1 + j.upper()

            count = count + 1
        ret_val.append(str_1)
    return tuple(ret_val)
myfunc_1("hai","bye","Hello","how","are","YOU")
```

    ('hai', 'bye', 'Hello', 'how', 'are', 'YOU')





    ('HaI', 'ByE', 'HeLlO', 'HoW', 'ArE', 'YoU')



## MAP
1. Used to iterate a function for the given number of inputs
2. It will iterate upto the minimum index value in list
3. Syntax

    map(function,input_para_1(iteration),.......,input_para_n(iteration))


```python
def name_map(n="NAME",a="AGE"):

        print(f"Default parameter \nName: {n}\nAge: {a}\n ")
        return "Success"
    
name_in =  ["Jim","Tom","Sam","kim"]
age_in = [22,32,56,30,26]
list(map(name_map,name_in,age_in))
```

    Default parameter 
    Name: Jim
    Age: 22
     
    Default parameter 
    Name: Tom
    Age: 32
     
    Default parameter 
    Name: Sam
    Age: 56
     
    Default parameter 
    Name: kim
    Age: 30
     





    ['Success', 'Success', 'Success', 'Success']



## FILTER
1. Similar to map function but it will return the value that has been inputed instead of boolean output.
2. It takes only two arguments
3. Syntax

    filter(function,input_para_1(iteration),.......,input_para_n(iteration)


```python
def check_eoo(num):
    return num%2 == 0
num = [1,2,3,4,5,6]
for i in filter(check_eoo,num):
    print(i)

print("\n***************\n")

for i in map(check_eoo,num):
    print(i)
```

    2
    4
    6
    
    ***************
    
    False
    True
    False
    True
    False
    True


## LAMBDA
1. Anonymous function
2. It is used to convert the simple functions into lambda function to save memory
3. syntax 

    1.lambda input values:operations (and returns the operation result)



```python
# basic use
print("\n******* basic use ********\n")
sq = lambda num:num*num
print(f"{sq(2)}")

print("\n******* using map 1 input ********\n")
# using map 1 input
ti_in = (1,2,3,4)
l_m_v = list(map(lambda num:num*num,ti_in))
print(f"{l_m_v}")

print("\n******* using map 2 input ********\n")
# using map 2 input
ti_in = (1,2,3,4)
li_in = (5,6,7,8)
l_m_v = list(map(lambda num1,num2:num1*num2,ti_in,li_in))
print(f"{l_m_v}")

print("\n******* Using tuple ********\n")
# using tuple
num_f = [1,2,3,4,5,6]
num_f_fil = tuple(filter(lambda num:num%2 == 0,num_f))
print(f"{num_f_fil}")

print("\n***************\n")

```

    
    ******* basic use ********
    
    4
    
    ******* using map 1 input ********
    
    [1, 4, 9, 16]
    
    ******* using map 2 input ********
    
    [5, 12, 21, 32]
    
    ******* Using tuple ********
    
    (2, 4, 6)
    
    ***************
    


## ALL AND ANY
1. All
    
    This function returns True if all the given inputs are true
2. Any
    
    This function returns True if any of the given inputs are true


```python
Boolean_val = [True,True,True,False]
all_v = all(Boolean_val)
any_v = any(Boolean_val)
print (f"print if all boolean value is true => {all_v}\nprint if any boolean value is true => {any_v}")
```

    print if all boolean value is true => False
    print if any boolean value is true => True


## VARIABLE PRIORITY'S
### LEGB
1. Local 

    Assigned inside the function or lambda
    
2. Enclosing function local

    It is the variable declared in the nested functions
    For example:
        function 1():
            var 1 | Enclosing function local
            function 2():
                var 2 | local function
    
3. Global

    Varriables assigned in top level of the module file or with "global" keyword.
    
4. Built-in 
    
    Variables which are built in like open range



```python
g_var = "\nGlobal variable\n"
def function_1():
    print(g_var) # Global Variable
    e_var = "\nLocal variable 1 (Enclosing function local)\n"
    def function_2():
        print(e_var) # Enclosing function local
        l_var = "\nLocal variable 2\n"
        print(l_var) # Local Variable
    function_2()
function_1()    

    
```

    
    Global variable
    
    
    Local variable 1 (Enclosing function local)
    
    
    Local variable 2
    


## GLOBAL KEYWORD
1. To define global variable inside a function (for local variable)
2. Syntax 

    global global_variable
    
    # Example
    
    global_variable = "some string"
    def  function_1():
        global global_variable
        global_variable = "Some string is re assigned globaly"


```python
global_variable_str = "some string"
global_variable_int = 1
def  function_1():
    global global_variable_str
    global global_variable_int
    global_variable_str = "Some string is reassigned globaly"
    global_variable_int = 10.25
    print(f"\nInside the function :\n\tglobal_variable_str = > {global_variable_str}\n\tglobal_variable_int => {global_variable_int}\n")
print(f"\nBefore calling the function:\n\tglobal_variable_str = > {global_variable_str}\n\tglobal_variable_int => {global_variable_int}\n")        
function_1()
print(f"\nAfter calling the function:\n\tglobal_variable_str = > {global_variable_str}\n\tglobal_variable_int => {global_variable_int}\n")
```

    
    Before calling the function:
    	global_variable_str = > some string
    	global_variable_int => 1
    
    
    Inside the function :
    	global_variable_str = > Some string is reassigned globaly
    	global_variable_int => 10.25
    
    
    After calling the function:
    	global_variable_str = > Some string is reassigned globaly
    	global_variable_int => 10.25
    


## OOPs

1. Python allows us to develop applications using Object Oriented approach.
2. It simulates the real world entity. So real world problems can be easily solved through oops.

3. Object

    - It is an real time entity that has state and behavior.
    
4. Class

    - Class can be defined as a collection of objects.
    - It is a logical entity that has some specific attributes and methods. 
    - class ClassName():  
        other operation-1 
        
        ......
        
        other operation - n
        
5. Attributes
    - Attributes are similar to constructor which has to be implemented when a class is declared and need to be used 
    - While calling attributes no need of parentheses ()
    - Takes atleast 1 argument(default argument) "self"
    - syntax
    
        def __ init __ (self,para,1...,paran):
    - __ __init__ __ 
        - It is the Constructor of the class and it called automatically wheninstence of the class is created   
        - It is the First method
    - __self__ is the instance of the object itself, can be any name by self is preferred as it's easy for future reference.
6. Class object attributes 
    - Defined inside the class
    - It can be called during run time
    - Not connected to self or instance
7. Method
    - Method is a function that is associated with an object.
    - It is called method when it is inside the class.
    - In Python, method is not unique to class instances. 
    - While calling methods parentheses () is needed
    - Takes atleast 1 argument(default argument) "self"
        - Self is used to refer outside arguments which is inside the class
    - syntax
    
        def method (self,para,1...,paran):


```python
class ClassName():
    pass
samp_class = ClassName()
print(f"Type of the samo_class => {type(samp_class)}")
```

    Type of the samo_class => <class '__main__.ClassName'>



```python
class Pet():
        def __init__(self):# taking the argument
            print("Nothing other than self")
my_pet = Pet()


```

    Nothing other than self



```python
class Pet():
    def __init__(self,animal,breed):# taking the argument
        self.pet_anmial = animal# Assigning to self attributes 
        self.pet_breed = breed# Assigning to self attributes 


my_pet = Pet(animal="Dog",breed="Lab") 
my_pet_animal = my_pet.pet_anmial
my_pet_breed = my_pet.pet_breed
print(f"Type of the Pet => {type(my_pet_animal)}\nAttributes of the my_pet => {my_pet_animal}\nAttributes of the my_pet => {my_pet_breed}")

my_pet = Pet("Cat","Abyssinian")
my_pet_list = my_pet.pet_anmial,my_pet.pet_breed
print(f"\nType of the Pet => {type(my_pet_list)}\nAttributes of the my_pet => {my_pet_list}")
```

    Type of the Pet => <class 'str'>
    Attributes of the my_pet => Dog
    Attributes of the my_pet => Lab
    
    Type of the Pet => <class 'tuple'>
    Attributes of the my_pet => ('Cat', 'Abyssinian')



```python
class Pet():
    Species = "MAMMAL" #Class object attributes 
    def __init__(self,animal,breed):# taking the argument
        self.pet_anmial = animal# Assigning to self attributes 
        self.pet_breed = breed# Assigning to self attributes
        

my_pet = Pet(animal="Dog",breed="Lab") 
my_pet_animal = my_pet.pet_anmial
my_pet_breed = my_pet.pet_breed
my_pet_Species = my_pet.Species
print(f"Type of the Pet => {type(my_pet_animal)}\nAttributes of the my_pet => {my_pet_animal}\nAttributes of the my_pet => {my_pet_breed}\nAttributes of the my_pet => {my_pet_Species}")

my_pet = Pet("Cat","Abyssinian")
my_pet_list = my_pet.pet_anmial,my_pet.pet_breed,my_pet.Species
print(f"\nType of the Pet => {type(my_pet_list)}\nAttributes of the my_pet => {my_pet_list}")
```

    Type of the Pet => <class 'str'>
    Attributes of the my_pet => Dog
    Attributes of the my_pet => Lab
    Attributes of the my_pet => MAMMAL
    
    Type of the Pet => <class 'tuple'>
    Attributes of the my_pet => ('Cat', 'Abyssinian', 'MAMMAL')



```python
class Pet():
        species = "MAMMAL" # Class object attributes 
        def __init__(self):# taking the argument
            print(self.species)# calling Class object attributes inside attribute to print
my_pet = Pet()



```

    MAMMAL



```python
class Pet():
    Species = "MAMMAL" #Class object attributes 
    my_name = "Mammal name" 
    def __init__(self,animal,breed):# taking the argument
        self.pet_anmial = animal# Assigning to self attributes 
        self.pet_breed = breed# Assigning to self attributes
    def sound_dog(self,name = my_name): # Method "Action/operations" && self is used to refer outside arguments of the class
        print(f"{self.pet_anmial}: {name} woooooooof")
    def sound_cat(self,name = my_name): # Method "Action/operations"
        print(f"{self.pet_anmial}: {name} Meeeeeeeow")
        
#DOG
my_pet = Pet(animal="Dog",breed="Lab") 
my_pet_animal = my_pet.pet_anmial
my_pet_breed = my_pet.pet_breed
my_pet_Species = my_pet.Species
print(f"Type of the Pet => {type(my_pet_animal)}\nAttributes of the my_pet => {my_pet_animal}\nAttributes of the my_pet => {my_pet_breed}\nAttributes of the my_pet => {my_pet_Species}")
my_pet.sound_dog()

#CAT
my_pet = Pet("Cat","Abyssinian")
my_pet_list = my_pet.pet_anmial,my_pet.pet_breed,my_pet.Species
print(f"\nType of the Pet => {type(my_pet_list)}\nAttributes of the my_pet => {my_pet_list}")
my_pet.sound_cat("Tom")
```

    Type of the Pet => <class 'str'>
    Attributes of the my_pet => Dog
    Attributes of the my_pet => Lab
    Attributes of the my_pet => MAMMAL
    Dog: Mammal name woooooooof
    
    Type of the Pet => <class 'tuple'>
    Attributes of the my_pet => ('Cat', 'Abyssinian', 'MAMMAL')
    Cat: Tom Meeeeeeeow



```python
class Circle():
    pi = 22/7
    
    def __init__(self,radius=1): # Default value for radius
        self.radius = radius
        self.circumference = self.pi*r*2
        # similar to self.radius
    def area(self,pi = pi):
        r = self.radius
        print(pi*(r**2))
        return pi*(r**2)
    def diameter(self):
        r = self.radius
        print(r*r)
        return r*r
cir = Circle(3)
cir.area()
cir.diameter()
cir.circumference
```

    28.285714285714285
    9





    4701.714285714285



## OOPs - INHERITANCE
1. It inherit the one class into another class.
2. Technically it inherit parent class into child class.
3. It has all the functionality of parent class and it can be overwritten.
4. Extra methods can be also added to child class
5. Syntax

    class Parent_class():
        ...
    class Child_class(Parent_class) 


```python
# Parent Class
class Animal(): 
    
    def __init__(self):
        print ("Animal class has been created (Parent class)")
    
    def eat(self):
        print("I can eat")
        
    def run(self):
        print("I can run")
        
    def i_am(self):
        print("I am an animal")
        
# Child Class
class Dog(Animal): 
    
    def __init__(self):
        print ("Dog class has been created (Child class)")
        Animal.__init__(self)
        print ("Animal class has been inherited into Dog class (Parent class Inherited into Child class)")
    def i_am(self):
        print("I am a Dog (i_am() method of the Animal class has been overwritten)")
        
dog = Dog()
dog.eat()
dog.run()
dog.i_am()
```

    Dog class has been created (Child class)
    Animal class has been created (Parent class)
    Animal class has been inherited into Dog class (Parent class Inherited into Child class)
    I can eat
    I can run
    I am a Dog (i_am() method of the Animal class has been overwritten)


## OOPs - POLYMOROHISM
1. Using same method name in different class. 
2. Methods are called using classes.


```python
class Dog(): 
    
    def __init__(self,name):
        self.name = name
        print ("I am a dog")
    def sound(self):
        print("\tI bark")
class Cat(): 
    
    def __init__(self,name):
        self.name = name
        print ("I am a cat")
    def sound(self):
        print("\tI purrf")
        
scooby = Dog("scooby")
tom = Cat("tom")
pets =[scooby,tom]
for pet in pets:
    print(f"\nI am {pet.name}")
    pet.sound()
```

    I am a dog
    I am a cat
    
    I am scooby
    	I bark
    
    I am tom
    	I purrf


## Abstract class
1. Abstract class has abstract methods.
2. Defying a method in base class, which can be used in future when a class is inherited.



```python
# Parent Class
class Animal(): 
    
    def __init__(self):
        print ("Animal class has been created (Parent class)")
    
    def eat(self):
        raise NotImplementedError("Not Implemented ")
    def run(self):
        print("I can run")
        
# Child Class
class Dog(Animal): 
    
    def __init__(self):
        print ("Dog class has been created (Child class)")
        Animal.__init__(self)
        print ("Animal class has been inherited into Dog class (Parent class Inherited into Child class)")
    def eat(self):
        print("I can eat (eat() method of the Animal class has been Implemented)")
        
dog = Dog()
dog.run()
dog.eat()
```

    Dog class has been created (Child class)
    Animal class has been created (Parent class)
    Animal class has been inherited into Dog class (Parent class Inherited into Child class)
    I can run
    I can eat (eat() method of the Animal class has been Implemented)


## SPECIAL METHODS
1. Special methods are also caled as Magic or Dunder
2. Syntax
    - For str
    
        def __ str __(self):
            operations


```python
class Dog(): 
    
    def __init__(self):
        print ("Dog class has been created")

    def eat(self):
        print("I can eat")
    def __str__(self):
        return "Dog"
    def __len__(self):
        return len("Dog")
    def __del__(self):
        print("Dog class has been deleted successfully")
        
dog = Dog()
dog.eat()
ln = len(dog)
st = str(dog)
print(f"When len method used: {ln}\nWhen str method used: {st}  ")
del dog
```

    Dog class has been created
    I can eat
    When len method used: 3
    When str method used: Dog  
    Dog class has been deleted successfully


### Updating Self value


```python
class Word_count(): 
    
    def __init__(self,count = 0):
        print ("Word_count class has been created\nInitial count value has been set to 0\nvalue of Count can be updated if neede")
        self.count = count
    def wordcount(self,wc):
        for w in (wc.split()):
            self.count = self.count + 1
        print(f"\nThe total number of words: {self.count}\n")
            
wc = Word_count()
wc.wordcount("Hello world this is a word count programme")


```

    Word_count class has been created
    Initial count value has been set to 0
    value of Count can be updated if neede
    
    The total number of words: 8
    



```python
%%writefile textfile.txt
Hello these are the text which will be inside the textfile.txt 
we can give any kind Of text inside
Line 1
Line 2
```

    Overwriting textfile.txt


## Modules and packages
1. Modules are the collection of pre-written python file which can have function or class which can be used in future by importing.
2. Packages are the collection of those modules(python file or its sub folders).
3. If we are placing the python file inside a folder __init__.py file should be placed in same folder which helps the python to identify it as packages.



```python
%%writefile hello_module.py 
# creating .py file
def print_me():
    print("Hello, I am  hello_module.py")
    
```

    Overwriting hello_module.py



```python
ls
```

    [34mComplete-Python-3-Bootcamp-master[m[m/     Python_A_-_Z_5_25_1.ipynb
    Complete-Python-3-Bootcamp-master.zip  Python_A_-_Z_5_25_2.ipynb
    Python_A_-_Z_1_16.ipynb                Python_A_-_Z_6_27_1.ipynb
    Python_A_-_Z_2_19_1.ipynb              Python_A_-_Z_7_28_1.ipynb
    Python_A_-_Z_2_19_2.ipynb              Untitled-Copy1.ipynb
    Python_A_-_Z_3_20_1.ipynb              Untitled.ipynb
    Python_A_-_Z_3_20_2.ipynb              Untitled1.ipynb
    Python_A_-_Z_4_21_1.ipynb              [34m__pycache__[m[m/
    Python_A_-_Z_4_21_2.ipynb              [34mhello_main_pack[m[m/
    Python_A_-_Z_4_21_2_back.ipynb         hello_module.py
    Python_A_-_Z_4_22_1.ipynb              textfile.txt
    Python_A_-_Z_4_23_1.ipynb



```python
# importing and printing from user Defined modules
from hello_module import print_me
print_me()
```

    Hello, I am  hello_module.py


#### - Creating and using a folder called hello _ main _ pack and hello _ main _ pack/hello _ sub _ pack
#### - Creating __ init __.py file in hello _ main _ pack and hello _ main _ pack/hello _ sub _ pack


```python
%%writefile hello_main_pack/__init__.py 
 
```

    Overwriting hello_main_pack/__init__.py



```python
%%writefile hello_main_pack/hello_sub_pack/__init__.py 
 
```

    Overwriting hello_main_pack/hello_sub_pack/__init__.py



```python
%%writefile hello_main_pack/hello_main_module.py 
# creating .py file
def print_me_main():
    print("Hello, I am  hello_main_module.py")
```

    Overwriting hello_main_pack/hello_main_module.py



```python
%%writefile hello_main_pack/hello_sub_pack/hello_sub_module.py 
# creating .py file
def print_me_sub():
    print("Hello, I am  hello_sub_module.py")
```

    Overwriting hello_main_pack/hello_sub_pack/hello_sub_module.py



```python
from hello_main_pack import hello_main_module
from hello_main_pack.hello_sub_pack import hello_sub_module

hello_main_module.print_me_main()
sub_mod = hello_sub_module
sub_mod.print_me_sub()
```

    Hello, I am  hello_main_module.py
    Hello, I am  hello_sub_module.py


## ERROR AND EXCEPTION HANDLING
1. Using this we can handel runtime error.
2. We can catch the exception or error with __except__ and do some operation with it.
3. We can avoid the total break down of the program using __finnaly__ method.
4. Else can be used when you need to some operation if there is no error
4. Syntax

    try:
        //...operations...//
    except: 
        //...operations...//
        .
        .
        .
    except:
        //...operations...//
        .
        .
        .
    else:
        //...operations...//  
    finally:
        //...operations...//


```python
while(True):
    num_dd = input("Enter a number the dividend0\n\n\t")
    num_dr = input("Enter a number the divisor\n\n\t")
    try:
        add_v = int(num_dd) / int(num_dr) 
        print("***************************************************")
        print(f"\nDivided value => {num_dd}/{num_dr} = {add_v}\n")
        print("***************************************************")
    except TypeError:
        print("\nFound a TypeError\n")
    except ValueError:
        print("\nFound ValueError Give an NUMBER as an input \n")
    except ZeroDivisionError:
        print("***************************************************")
        print("\nAnything divided by zero is undefined \n")
        print("***************************************************")
        break
    except:
        print("\nFound one exception\n")
        break
    else:
        print("You successfully completed a Division")
        break
    finally:
        print("\nThank you for trying\n")
```

    Enter a number the dividend0
    
    	0
    Enter a number the divisor
    
    	8
    ***************************************************
    
    Divided value => 0/8 = 0.0
    
    ***************************************************
    You successfully completed a Division
    
    Thank you for trying
    


## RETURNING A FUNCTION

function1():

    function2():
    
    //....operations....//
    
    return function2


```python
def hello():
    print("Hello this is a Greeting message ")
    def bye():
        print("This is a message for send off")
    return bye # returning a function
bye_r = hello()

```

    Hello this is a Greeting message 



```python
bye_r() # returned function
```

    This is a message for send off


## PASSING A FUNCTION
function1():
    
    //....operations....//
    
function2(function1_in):
    
    function1_in()
    
    //....operations....//
    
function2(function1)


```python
# Function 1
def input_int():
    while(True):   
        try:
            inp_i = int(input())
            return inp_i
            break
        except ValueError:
            print(f"\n please give an Number\n")
```


```python
# Function 2
def address(num_int): # reciving the function
    print("Please Enter your Address")
    address = input() 
    print("Please Enter your Phone number")
    phone_num = num_int() # calling the function
    
    print(f"\nYour Address :\n\t{address}\nYour Phone Number: \n\t{phone_num}")
    

```


```python
address(input_int) # passing the function
```

    Please Enter your Address
    458, gbhxb, hbhbsf,b 83764, zx
    Please Enter your Phone number
    286367385
    
    Your Address :
    	458, gbhxb, hbhbsf,b 83764, zx
    Your Phone Number: 
    	286367385


## DECORATORS
1. used to wrap the functions
2. Using the @ symbol and the function name needed to be added and this should be mentioned above the function that has to be added with.
3. Commenting or removing the @ line will unwrap the function
4. syntax

        function1(function2_in):
            wrap_fun():
                function2_in():
                     //....operations....//
            //....operations....//
            
            return wrap_fun
        
        @function1
        function2():


            //....operations....//

        function2()




```python
def hello_fun(in_func):
    def wrap_func():
        in_func()
        print("hello world => bye_fun() is executed, to combine both properties/nIf not executed it will have only hello_fun() Properties")
        print("The wrap_func should be returend to give the combiend properties of two functions")
    return wrap_func

```


```python
@hello_fun
def bye_fun():
    print("Good Bye")
```


```python
bye_fun()
```

    Good Bye
    hello world => bye_fun() is executed, to combine both properties/nIf not executed it will have only hello_fun() Properties
    The wrap_func should be returend to give the combiend properties of two functions



```python
#@hello_fun
def bye_fun():
    print("Good Bye")
bye_fun()
```

    Good Bye


## GENERATOR FUNCTIONS
1. It will generate a sequence value.
2. It computes one value and Wait for another value to be called to compute. 
3. Using generator function we can reduce the Memory consumption.
4. Keywords
    - yield
    - next()
    - iter()


## YIELD
1. It Collect the sequence of value like adding value to list.
2. It is more efficient in terms of memory compared to list.
3. Yield are used in Python generators
4. It is similar to return
5. Syntax

    yield value


```python
def y_t(in_v):
    for i in range(1,in_v):
        yield i**10 # using yield to collect value
```


```python
print(list(y_t(10))) # Casting to list and Printing the value
```

    [1, 1024, 59049, 1048576, 9765625, 60466176, 282475249, 1073741824, 3486784401]


## NEXT 
1. It gives the value by remembering the privious value it given.
2. It will give StopIteration error if there is no value.


```python
lis_val = y_t(10)
```


```python
while(True):
    n_v = next(lis_val)
    print(n_v)
```

    1
    1024
    59049
    1048576
    9765625
    60466176
    282475249
    1073741824
    3486784401



    ---------------------------------------------------------------------------

    StopIteration                             Traceback (most recent call last)

    <ipython-input-228-c860c83fe7d3> in <module>()
          1 while(True):
    ----> 2     n_v = next(lis_val)
          3     print(n_v)


    StopIteration: 


## ITER 
1. This function convert the variable to generator type
2. syntax
    
    iter(value)


```python
next(list(y_t(10)))
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-229-c455fd3b8e10> in <module>()
    ----> 1 next(list(y_t(10)))
    

    TypeError: 'list' object is not an iterator



```python
next(iter(list(y_t(10))))
```




    1



## COLLECTIONS MODULE
1. IT has many datatype which is very Useful for programing
2. Datatypes
    - Counter
        - Counts the number of occurrence and return the result.
    - defaultdict
        - Avoids key error by adding by itself in a given range
    - orderdict
        - It will remember the order of the key and value.
    - namedtuple
        - It is used to call the tuple with name instead of using index.


```python
from collections import Counter
a_list = [1,1,1,3,1,1,5,7,8,4,6,3,7,8,7,3,5,7,6,6,4,3,2,9,0,5]

a_counter = Counter(a_list)
print(a_counter)
```

    Counter({1: 5, 3: 4, 7: 4, 5: 3, 6: 3, 8: 2, 4: 2, 2: 1, 9: 1, 0: 1})



```python
# Word count
st = "Hello world and new world"
st = st.split()
wc = Counter(st)
```


```python
a_counter_m = a_counter.most_common(2) # returns top two most common values
a_counter_k = a_counter.keys() # Returns only the key
a_total_num = sum(wc.values()) # Counting the total number of words
print(f"a_counter_m => {a_counter_m}\na_counter_k => {a_counter_k}\na_total_num => {a_total_num}")
```

    a_counter_m => [(1, 5), (3, 4)]
    a_counter_k => dict_keys([1, 3, 5, 7, 8, 4, 6, 2, 9, 0])
    a_total_num => 5



```python
# Defaultdict
from collections import defaultdict
d_dict = defaultdict(lambda:random.randint(1,100))
d_dict["hai"]
d_dict[1]
d_dict
```




    defaultdict(<function __main__.<lambda>()>, {'hai': 100, 1: 82})




```python
#Order Dictionary 
from collections import OrderedDict
o_dict = OrderedDict()
o_dict[1] = "a"
o_dict[2] = "b"
o_dict[3] = "c"
o_dict[4] = "d"
o_dict[5] = "e"
o_dict[6] = "f"
o_dict[7] = "g"
for k,v in o_dict.items():
    print(f"Key => {k}\tValues => {v}")
```

    Key => 1	Values => a
    Key => 2	Values => b
    Key => 3	Values => c
    Key => 4	Values => d
    Key => 5	Values => e
    Key => 6	Values => f
    Key => 7	Values => g



```python
from collections import namedtuple
dog = namedtuple("dog","sound Breed colour")
```


```python
dog_nt = dog(sound = "bsrk", Breed = "Lab",colour = "Black" )
```


```python
dog_nt_index = dog_nt[1]
dog_nt_name = dog_nt.Breed
print(f"Using index => {dog_nt_index}\nUsing Name => {dog_nt_name}")
```

    Using index => Lab
    Using Name => Lab


## DATE AND TIME



```python
# date and time
import datetime
t = datetime.time(5,21,1,3)
print(t)
print(f"Hour => {t.hour}\nMicrosecond = > {t.microsecond}")

```

    05:21:01.000003
    Hour => 5
    Microsecond = > 3



```python
print (datetime.time.min) # print's minimum time in a day 
print (datetime.time.max) # print's maximum time in a day 
```

    00:00:00
    23:59:59.999999



```python
date_in = datetime.date(2017,3,4)
print(date_in) # print's Date
print(date_in.day) # print's Day
print(date_in.month) # print's Month
print(date_in.year) # print's Year
print(datetime.date.min) # print's Min date
print(datetime.date.max) # print's Max date
```

    2017-03-04
    4
    3
    2017
    0001-01-01
    9999-12-31


## TIMEIT
1. to check the time of your code


```python
import timeit
time_n_l = timeit.timeit('"-".join(str(n) for n in range (100))', number=10000)
time_l = timeit.timeit('"-".join([str(n) for n in range (100)])', number=10000)
print(f"Time taken by code (non list) => {time_n_l}\nTime taken by code (list) => {time_l}")
```

    Time taken by code (non list) => 0.30248554199988575
    Time taken by code (list) => 0.20334017499953916

