# Input/Output

## STD I/O

### STD Library

The **STD** is the **STANDARD** library used in UPL to do everything, you can theoretically do everything ine STD, but the complexity will increase that way. That's why other libraries are built on top(and only on top) of **STD**!

To import the STD Library we can use:

```upl
import std.l
```

The `import` is a function to include a *library* into your file. The oposite is `export` to include a *framework*.  
The main difference is that *import* extends **your code** relative to the library, and *export* extends **the framework** relative to your code!  

The second argument that comes after import/export are the libraries/frameworks. If there is more than one library/framework, you should separate them with a comma: `import std.l, foo.l, bar.l`  
Libraries end with `.l` while frameworks dont have any extensions!  

### STD I/O

To use the STD I/O you can do this:
```upl
import std.l

std:out << "Hello World!"
```
Or you can import STD as the standard library, eliminating the neet to call it every time:
```upl
import std.l as standard

out << "Hello World!"
```
The way that I/O works in STD is tha almost the same way as the [linux data streams](https://www.howtogeek.com/435903/what-are-stdin-stdout-and-stderr-on-linux/) work. Redirections also work the same thats why we use `<<`, to append output!

To take input and output it imediately:
```upl
import std.l

std:in >> std:out
```
This works by redirecting the input to the output!
To store the data somewhere, you need to first create a variable or a file:
```upl
import std.l

var myVariable

std:in >> var
std:out << var
```
```upl
import std.l

addr myFile = "./text.txt"

std:in >> myFile
std:out << myFile
```
Note how `var` can store variable information(like int, tring, float, etc) while `addr` can store addresses(like file locations, storage locations, memory addresses, etc)!
