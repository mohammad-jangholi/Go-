
Go file consists of the following parts:

- Package declaration
- Import packages
- Functions
- Statements and expressions

example 


```
package main 
import "fmt" 

func main() { 
  fmt.Println("Hello World!")
} 
```


package main >>> part of a package
import "fmt"  >>> lets us import files
func main() {} >>> s a function. Any code inside its curly brackets `{}` will be executed
fmt.Println() >>> is a function made available from the  fmt



statments :

- The left curly bracket `{` cannot come at the start of a line
- In Go, statements are separated by ending a line (hitting the Enter key) or by a semicolon "`;`"




variables :

there are two ways to declare a variable

Use the `:=` sign 

```
_variablename_ := _value_
```

Use the `var` keyword

```
var _variablename type_ = _value_
```


example

```
package main
import "fmt"

func main() {
  var student1 string = "John" _//type is string_
  var student2 = "Jane" _//type is inferred_
  x := 2 _//type is inferred_

  fmt.Println(student1)
  fmt.Println(student2)
  fmt.Println(x)
  }
```


## Difference Between var and :=


| var                                                                  | :=                                                                                                      |
| -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| Can be used **inside** and **outside** of functions                  | Can only be used **inside** functions                                                                   |
| Variable declaration and value assignment **can be done separately** | Variable declaration and value assignment **cannot be done separately** (must be done in the same line) |


can use var in multi 

Declaration in a Block

```
var (
     a int
     b int = 1
     c string = "hello"
   )
```



const varible 


The `const` keyword declares the variable as "constant", which means that it is **unchangeable and read-only**.

```
const _CONSTNAME type_ = _value_
```


```
package main
import "fmt"

const PI = 3.14

func main() {
  fmt.Println(PI)
}
```


Go has three functions to output text

- `Print()` : The `Print()` function prints its arguments with their default format.

```
package main
import "fmt"

func main() {
  var i,j string = "Hello","World"

  fmt.Print(i)
  fmt.Print(j)
}
```

> [!NOTE]
> `HelloWorld`

- `Println()` : The `Println()` function is similar to `Print()` with the difference that a whitespace is added between the arguments, and a newline is added at the end

- `Printf()`

----------------------

comparison operators :

| Operator | Name           | Description                            | Example |
| -------- | -------------- | -------------------------------------- | ------- |
| +        | Addition       | Adds together two values               | x + y   |
| -        | Subtraction    | Subtracts one value from another       | x - y   |
| *        | Multiplication | Multiplies two values                  | x * y   |
| /        | Division       | Divides one value by another           | x / y   |
| %        | Modulus        | Returns the division remainder         | x % y   |
| ++       | Increment      | Increases the value of a variable by 1 | x++     |
| --       | Decrement      | Decreases the value of a variable by 1 | x--     |



| Operator | Example | Same As    |
| -------- | ------- | ---------- |
| =        | x = 5   | x = 5      |
| +=       | x += 3  | x = x + 3  |
| -=       | x -= 3  | x = x - 3  |
| *=       | x *= 3  | x = x * 3  |
| /=       | x /= 3  | x = x / 3  |
| %=       | x %= 3  | x = x % 3  |
| &=       | x &= 3  | x = x & 3  |
| \|=      | x \|= 3 | x = x \| 3 |
| ^=       | x ^= 3  | x = x ^ 3  |
| >>=      | x >>= 3 | x = x >> 3 |
| <<=      | x <<= 3 | x = x << 3 |


| Operator | Name                     | Example |
| -------- | ------------------------ | ------- |
| ==       | Equal to                 | x == y  |
| !=       | Not equal                | x != y  |
| >        | Greater than             | x > y   |
| <        | Less than                | x < y   |
| >=       | Greater than or equal to | x >= y  |
| <=       | Less than or equal to    | x <= y  |

--------------


logical operators 

| Operator | Name        | Description                                             | Example            |
| -------- | ----------- | ------------------------------------------------------- | ------------------ |
| &&       | Logical and | Returns true if both statements are true                | x < 5 &&  x < 10   |
| \|\|     | Logical or  | Returns true if one of the statements is true           | x < 5 \|\| x < 4   |
| !        | Logical not | Reverse the result, returns false if the result is true | !(x < 5 && x < 10) |


-----

## Bitwise Operators

| Operator | Name                 | Description                                                                                             | Example |
| -------- | -------------------- | ------------------------------------------------------------------------------------------------------- | ------- |
| &        | AND                  | Sets each bit to 1 if both bits are 1                                                                   | x & y   |
| \|       | OR                   | Sets each bit to 1 if one of two bits is 1                                                              | x \| y  |
| ^        | XOR                  | Sets each bit to 1 if only one of two bits is 1                                                         | x ^ b   |
| <<       | Zero fill left shift | Shift left by pushing zeros in from the right                                                           | x << 2  |
| >>       | Signed right shift   | Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off | x >> 2  |


-----

## Go Conditions


- Less than `<`
- Less than or equal `<=`
- Greater than `>`
- Greater than or equal `>=`
- Equal to `==`
- Not equal to `!=`
- Logical AND `&&`
- Logical OR `||`
- Logical NOT `!`


| Example            |
| ------------------ |
| x > y              |
| x != y             |
| (x > y) && (y > z) |
| (x == y) \|\| z    |


-------------

## Go Maps

Maps are used to store data values in key:value pairs.




```
package main
import "fmt"


func main() {
  var a = make(map[string]string) _// The map is empty now_
  a["brand"] = "Ford"
  a["model"] = "Mustang"
  a["year"] = "1964"
                                 _// a is no longer empty_
  b := make(map[string]int)
  b["Oslo"] = 1
  b["Bergen"] = 2
  b["Trondheim"] = 3
  b["Stavanger"] = 4

  fmt.Printf("a\t%v\n", a)
  fmt.Printf("b\t%v\n", b)
}
```

