# PyDLLs
Python Double Linked Lists utility, supporting Multiple Double Linked Lists 

## Simple Double Linked List
### Interface required:

#### Linked List class must have attributes:
* lltail (tail node linker)
* llhead (head node linker)

#### Node class must have attributes:
* llprev (previous node linker)
* llnext (next node linker)
#### Node class must have methods (for debug):
* __int__(self)



## Double Linked Lists with Arrays

Tagged Linked List, useful to maintain original values and link them at the same moment through different Double Linked Lists.
With the same instances, you could organize different Double Linked List, one for each chosen tag.
### Interface required:

#### Linked List class must have these arrays:
* llheads = [None, None, None....] (head node linkers, one for each list)
* lltails = [None, None, None....] (tail node linkers, one for each list)
#### Node class must have these arrays:
* nexts = [None, None, None, ...] =  (next node linkers, one for each list)
* prevs = [None, None, None, ...] =  (previous node linkers, one for each list)
* indexes = [None, None, None, ...] =  (index of node, one for each list)
#### Node class must have methods (for debug):
* __int__(self)



### Example:
Nodes are just 5. Class of these object is not important. It's necessary that this class has as parameter three arrays,
called nexts, prevs and indexes with lenght the number of list to support.
We can ipotize that these elements are cars. A car has these parameters: gasoline level (0,100) and speed (0,120)
This tool can organize these 5 objects in a double linked list sorted by ascending gasoline level and a double linked list sorted by ascending speed at the same time.





## Double Linked Lists with Dictionary -- Deprecated (Arrays are better)

Tagged Linked List, useful to maintain original values and link them at the same moment through different Double Linked Lists-
With the same instances, you could organize different Double Linked List, one for each chosen tag.
### Interface required:

#### Linked List class must have these dictonary entries:
* lists["tag" + "head"] = (head node linker)
* lists["tag" + "tail"] (tail node linker)

#### Node class must have these dictonary entries:
* pointer["tag" + "prev"] =  (previous node linker)
* pointer["tag" + "next"] =  (next node linker)
* pointer["tag" + "index"] =  (index of this list)
#### Node class must have methods (for debug):
* __int__(self)


### Example:
Nodes are just 5. Class of these object is not important. It's necessary that this class has as parameter a dictonary called "pointer"
We can ipotize that these elements are cars. A car has these parameters: gasoline level (0,100) and speed (0,120)
This tool can organize these 5 objects in a double linked list sorted by ascending gasoline level and a double linked list sorted by ascending speed at the same time.


