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


| Value Types   | Reference Types |
| ------------- | ------------- |
| int  | slices  |
| float  | maps  |
| string  | channels  |
| bools  | pointers  |
| structs  | functions  |
<br>
Values types 
- Use pointers to change things in a function	<br>
Reference Types
- Don't worry about pointers

## Arrays vs Slices
Arrays
* Primitive data structure
* can't be resized
* rarely used directly

Slices
* Can grow and shrink
* Used 99% of the time for lists of elements

## Maps vs Structs 

| Maps   | Sturcts |
| ------------- | ------------- |
| All *keys* must be the same type.             All the *values* must be the same type | Values can be of differeent type   |
| Use to represent a collection of related propert  | You need to know all the different fields at compile time  |
| Don't need to know all the keys at compile time  | Keys don't support indexing   |
| keys are indexed - we can iterate over them  | use to represent a "thing" with a lot of differeent properties  |
| reference type!  | Value Type!  |


## Interfaces

We use interfaces to define a method set or a function set.
We're kind of defining what something of type is but what different functions and return types it should
have.
 
## Concurrency vs Parallelism

| Concurrency    | Parallelism |
| ------------- | ------------- |
| <img width="751" alt="Screenshot 2020-06-19 at 10 49 42" src="https://user-images.githubusercontent.com/57540755/85120853-bd6b2c00-b21b-11ea-9f2f-c4157732ec95.png"> | <img width="859" alt="Screenshot 2020-06-19 at 10 59 53" src="https://user-images.githubusercontent.com/57540755/85121056-0fac4d00-b21c-11ea-9735-812ba1626948.png">
 
 
 ## Channels
 The process of a Channel, connects all the Go routines to the main go channel function. Like so in the diagram below
 <img width="565" alt="Screenshot 2020-06-19 at 11 43 48" src="https://user-images.githubusercontent.com/57540755/85124658-2d7cb080-b222-11ea-9971-24c7bd452c84.png">
 - Channels are of type as well which means they can only send and receive of the same type, Int to Int, string to string for example. So these have to be declared when created.
 <br>
 How to send information to a channel
 <br>
<img width="808" alt="Screenshot 2020-06-19 at 13 44 08" src="https://user-images.githubusercontent.com/57540755/85133643-fb277f00-b232-11ea-9186-f4df79b5c430.png">



 
 






