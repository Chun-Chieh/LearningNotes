# Swift

- Basics
	- [Constans and Variables](https://github.com/chunchiehliang/LearningNotes/tree/master/Swift#constants-and-variables)
	- [Optionals](https://github.com/chunchiehliang/LearningNotes/tree/master/Swift#optionals)
	- [String Interpolation](https://github.com/chunchiehliang/LearningNotes/tree/master/Swift#string-interpolation)
	- [Functions](https://github.com/chunchiehliangh/LearningNotes/tree/master/Swift#functions)
- Classes and Objects
	- [Inheritance](https://github.com/chunchiehliang/LearningNotes/tree/master/Swift#inheritance)

## Basics

### Constants and Variables

```swift
var x = 3 // var x: Int = 3
x = 10
let x = 87
let arr = ["orange", "peach"]
let dict = ["banana" : "yellow", "kiwifruit" : "green"]
```

### Optionals

```swift
var x: String?
x = "Foo"
print(x!) // Force unwrapping
```
#### Null/Nil Handler

In Swift, ```Optional binding``` is used to handle nil pointer.
```swift
var msg: String?
if let existingMsg = msg {
  // assign msg to existingMsg when it's not nil, and then print it out
  print(existingMsg)
}
```

### String Interpolation

```swift
print("I'm \(myAge) years old")
print("Good morning, \(user.name)")
```

### Functions

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

