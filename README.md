# Kotlin & Swift (& Java) 

- Basics
	- [Constans and Variables](https://github.com/chunchiehliang/LearningNotes#constants-and-variables)
	- [Optionals](https://github.com/chunchiehliang/LearningNotes#optionals)
	- [String Interpolation](https://github.com/chunchiehliang/LearningNotes#string-interpolation)
	- [Functions](https://github.com/chunchiehliang/LearningNotes#functions)
- Classes and Objects
	- [Inheritance](https://github.com/chunchiehliang/LearningNotes#inheritance)

## Basics

Java
```java
System.out.println("Hello World!")
```
Kotlin
```kotlin
println("Hello World!")
```
Swift
```Swift
print("Hello World")
```

### Constants and Variables
Kotlin uses ```val``` to define constants while Swift uses ```let```.

java
```java
int x = 3
x = 10
final static int constant = 87
```
Kotlin
```kotlin
var x = 3 // var x: Int = 3
x = 10
val x = 87
```
Swift
```swift
var x = 3 // var x: Int = 3
x = 10
let x = 87
```

### Optionals
Kotlin
```kotlin
var x: String? = null // variables are required to initialzed in Kotlin
x = "Foo"
println(x!!) // Force unwrapping
```
Swift
```swift
var x: String?
x = "Foo"
print(x!) // Force unwrapping
```
#### Null/Nil Handler
In Kotlin, you can either use if-else to check null pointer,
```kotlin
var msg: String?
if (msg != null) println("Message: $msg") else println("it's null")
```
or use ```safe call```operator (```Elvis Operator```).
```kotlin
println(msg ?: "it's null")
```

In Swift, ```Optional binding``` is used to handle nil pointer.
```swift
var msg: String?
if let existingMsg = msg {
  // assign msg to existingMsg when it's not nil, and then print it out
  print(existingMsg)
}
```

### String Interpolation

Java
```java
System.out.println(String.format("I'm %d years old", myAge))
System.out.println(String.format("Good morning, %s", user.getName()))
```
Kotlin
```kotlin
println("I'm $myAge years old")
println("Good morning, ${user.name}")
```
Swift
```swift
print("I'm \(myAge) years old")
print("Good morning, \(user.name)")
```

### Functions

Java has ```default``` 'default' access modifier, which allows access within the same package.

```java
static String addTwoNumbers(int num1, int num2) {
  return num1 + num2
}
addTwoNumbers(8, 9)
```

In Kotlin, the 'default' visibility is ```public``` which is accessible everywhere.

**Getters always have the same visibility as the property**

```kotlin
fun addTwoNumbers(num1: Int, num2: Int): Int {
  return num1 + num2
}
addTwoNumbers(8, 9)
```
It can also be written in one line.
```kotlin
fun addTwoNumbers(num1: Int, num2: Int) = num1 + num2
```

Swift has ```internal``` as 'default' access modifier which allows access within the same module

```swift
func addTwoNumbers(num1: Int, num2: Int) -> Int {
  return num1 + num2
}
addTwoNumbers(num1: 8, num2: 9)
```

## Classes and Objects
Swift
```swift
class Animal {
  var age = 0
  convenience init (age: Int) {
  self.init()
  self.age = age
  }

  func breathe() {
	// ...
  }
}
```

### Inheritance

Swift
```swift
class Mammal: Animal {
  override func breathe() {
  // ...
  }
}
```

