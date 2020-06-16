# GoLang_CheatSheet
Learning the basics GoLang just some pointers from the very start.

Basics defining Variables 

var fruit string
string = "apple"

var fruit string = "apple" 

<br>

the Go compiler automatically infers the variable data type example string

var fruit = "apple"

fruit := "apple"


## Data types 
* String
* Bool<br>
***Numeric types***
* uint8       the set of all unsigned  8-bit integers (0 to 255)
* uint16      the set of all unsigned 16-bit integers (0 to 65535)
* uint32      the set of all unsigned 32-bit integers (0 to 4294967295)
* uint64      the set of all unsigned 64-bit integers (0 to 18446744073709551615)
* int8        the set of all signed  8-bit integers (-128 to 127)
* int16       the set of all signed 16-bit integers (-32768 to 32767)
* int32       the set of all signed 32-bit integers (-2147483648 to 2147483647)
* int64       the set of all signed 64-bit integers (-9223372036854775808 to 9223372036854775807)
* float32     the set of all IEEE-754 32-bit floating-point numbers
* float64     the set of all IEEE-754 64-bit floating-point numbers
* complex64   the set of all complex numbers with float32 real and imaginary parts
* complex128  the set of all complex numbers with float64 real and imaginary parts
* byte        alias for uint8
* rune        alias for int32

# For each Loop
Standard Loop  results 
strings := []string{"hello", "world"}
for i, s := range strings {
    fmt.Println(i, s)
} // hello world

Underscores can be used for when we don't want to use the variables 
before 
for i, suits := range cardSuits {
		for j, values := range cardValues {
			cards = append(cards, values+" of "+suits)
		}

	}
	return cards
  After this will return the result of values and suits into our cards variable
for _, suits := range cardSuits {
		for _, values := range cardValues {
			cards = append(cards, values+" of "+suits)
		}

	}
	return cards

## Byte slice 

 greeting :=  "Hi there"    string value
    fmt.Println([]byte(greeting))
                 ↓
[72 105 32 116 104 101 114 101 33] byte slice


# FMT Package
Difference between Print and Println Used to print in terminal 
fmt.Print("I", "am", "hungry")
// Iamcool
fmt.Println("I", "am", "hungry")
// I am cool

Scan used to grab user input in terminal 
fmt.Scan(&name)
fmt.Print.f ("My name is %v)
// "My name is Jack"

## Verbs

* %v represents the named value in its default format
* %d expects the named value to be an integer type
* %f expects the named value to be a float type
* %2f Shows float time 2  decimal places 
* %T represents the type for the named value
* %t	the word true or false


## Struct and Pointers 
`waynePointer := &wayne`<br>
	`waynePointer.updateName("Paul")`<br>
	`wayne.print()`
`}"`

&Varible - Gives acess to the memory address of the value this variable is pointing at.

`*pointer` Gives the value of the memory address is pointing at 

IF a * is where a type is, it points at the type's information, an example struct `*person` might be in a receiver function which meants it will great the informations type name,surname etc. A description of a type.
<br>
Otherwise If the  pointer is like so  `*pointertoperson` It meants we want to manipulate the value for example change the value in the Persons type, E.g Name or surname change.


## Arrays vs Slices
Arrays
* Primitive data structure
* can't be resized
* rarely used directly

Slices
* Can grow and shrink
* Used 99% of the time for lists of elements

 







