# 🔹 Learn Dart (Flutter's Programming Language)

Welcome to the Dart programming language lecture! Dart is the primary language used in Flutter, a popular UI toolkit for building natively compiled applications across mobile, web, and desktop from a single codebase.

---

## 📌 1. Variables & Data Types

### ➤ Variables
```dart
var name = 'ABCD';
int age = 18;
double weight = 72.5;
bool isStudent = true;
String city = 'Bcdef';
```

### ➤ Data Types
- **int**: Integer values (`int a = 10;`)
- **double**: Decimal values (`double b = 10.5;`)
- **String**: Text (`String s = 'Hello';`)
- **bool**: Boolean values (`bool flag = true;`)
- **var**: Dynamically typed variable
- **dynamic**: Type changes at runtime

---

## 📌 2. Functions & Operators

### ➤ Functions
```dart
void greet(String name) {
  print('Hello, \$name!');
}

int add(int a, int b) => a + b;
```

### ➤ Operators
- **Arithmetic**: `+`, `-`, `*`, `/`, `%`
- **Relational**: `==`, `!=`, `>`, `<`, `>=`, `<=`
- **Logical**: `&&`, `||`, `!`
- **Assignment**: `=`, `+=`, `-=`, `*=`, `/=`

---

## 📌 3. Control Flow Statements

### ➤ if-else
```dart
if (age > 18) {
  print('Adult');
} else {
  print('Minor');
}
```

### ➤ Loops
- **for loop**:
```dart
for (int i = 0; i < 5; i++) {
  print(i);
}
```
- **while loop**:
```dart
int i = 0;
while (i < 5) {
  print(i);
  i++;
}
```
- **do-while loop**:
```dart
int i = 0;
do {
  print(i);
  i++;
} while (i < 5);
```

---

## 📌 4. Object-Oriented Programming

### ➤ Classes & Objects
```dart
class Person {
  String name;
  int age;

  Person(this.name, this.age);

  void showDetails() {
    print('Name: \$name, Age: \$age');
  }
}

void main() {
  Person p = Person('Joel', 19);
  p.showDetails();
}
```

### ➤ Inheritance
```dart
class Animal {
  void eat() => print('Animal eats');
}

class Dog extends Animal {
  void bark() => print('Dog barks');
}
```

### ➤ Polymorphism
```dart
class Shape {
  void draw() => print('Drawing shape');
}

class Circle extends Shape {
  @override
  void draw() => print('Drawing circle');
}
```

---

## 📌 5. Asynchronous Programming

### ➤ Futures & async-await
```dart
Future<String> fetchData() async {
  await Future.delayed(Duration(seconds: 2));
  return 'Data loaded';
}

void main() async {
  print('Fetching data...');
  String data = await fetchData();
  print(data);
}
```

### ➤ Streams
```dart
Stream<int> numberStream() async* {
  for (int i = 1; i <= 5; i++) {
    await Future.delayed(Duration(seconds: 1));
    yield i;
  }
}

void main() {
  numberStream().listen((number) {
    print('Received: \$number');
  });
}
```

---

Happy Learning Dart! 🚀
