# Codecademy: Java

### Introduction to Java

- Print: `System.out.println("text");`

- Data types:

  - `int` : Values between -2,147,483,648 and 2,147,483,647

  - `bool` : Either `true` or `false`

  - `char` : A single character, must be enclosed in single quotes, e.g. 'g'

- Variable: Store a value and must have a specified data type.

  - E.g. `int num = 7;`

- Whitespace is ignored in Java and is used to make code more presentable.

- Comments

  - Single line comment: `// comment`

  - Multi-line comment: 

    ```java
    /*
        here's another comment
        continuation of that comment
    */
    ```

- Math: `+, - , *, /`

  - Modulo `%` : Finds the remainder of a divison

- Relational operators: `<, <=, >, >=`

  - Used to compare data types have that defined ordering, like numbers.

  - Always returns a boolean (true/false)

- Equality operators: `==, !=`

  - Operands can be different data types

  ```java
  int num = 7;
  int bool = true;
  System.out.println(num == bool); // false
  ```

---

### Conditionals and Control Flow

- Boolean operators: `&&, ||, !` (and, or, not)

  - Precedence (order of evaluation)): 1) `!`. 2) `&&`, 3) `||`

- If-else statements

```java
if (...){
  ...
} else if (...){
  ...
} else {

}
```

- Ternary conditional
  - Shorter if/else statemen that returns a value depending on the result of a boolean expression

```java
int points = 21;
char result = (points > 20) ? 'win' : 'loss'; // win
```

- Switch statement

```java
switch(var){

  case 1: ...
    break;

  case 2: ...
    break;

  default: ...
      break;
}
```

---

### Object-Oriented Java

- Classes

  - Need to create a class constructor, otherwise Java will use one that doesn't allow for initialization.

  - Instance of a class = object

  - `void` keyword: No method is returned by the method

  - **Inheritance**: Allows classes to inherit behavior from another class.

Example of a class:

```java
class Car extends Vehicle { // Car objects can use methods defined in the Vehicle class
  
  // Instance variables
  int modelYear;
  
  // Constructor
  public Car(int year){ // year is a parameter to the constructor
    modelYear = year;
  }
  
  // Methods
  public void startEngine(){
    System.out.println("Vroom!");
  }
  
  public void drive(int distanceInMiles){
    System.out.println("Miles driven: " + distanceInMiles);
  }
  
  public int numberOfTires(){ // method that returns an int
    return 4;
  }
  
  public static void main(String[] args){
    Car myFastCar = new Car(2007); // creating an instance of Car object
    myFastCar.startEngine(); // calling the startEngine() method on the myFastCar object
    myFarCar.drive(14);
  }
}
```

```java
class Vehicle {
  
  public void checkBatteryStatus() {
    
    System.out.println("The battery is fully charged and ready to go!");
  }
}
```

---

### Data Structures

- For loop

```java
for(int counter = 0; counter < 5; counter++){
  ...
}
```

- ArrayList: 

  - Pre-defined Java class. Need to create an ArrayList object to use.

  - Stores a list of data of a specified type.

  - Starts with an index of 0.

```java
ArrayList<Integer> guizGrades = new ArrayList<Integer>();
quizGrades.add(95);
quizGrades.add(87);
quizGrades.add(0, 100); // Inserts value of 100 at index 0, shifting the indices of the rest of the elements in the ArrayList by one

System.out.println(quizGrades.get(0)); //Gets the value at index 0

for(int i = 0; i < quizGrades.size(); i++){ // `size` method returns an int w/ the total elements in the ArrayList
  System.out.println(quizGrades.get(i));
}
```

- For Each Loop

  - Shortcut for a for loop

```java
for(Integer grade: quizGrades){ // where `grade` is the iterator and `quizGrades is the ArrayList`
  System.out.println(grade);
}
```

- HashMap

  - Contains a set of keys and a value for each key

  ```java
  HashMap<String, Integer> myFriends = new HashMap<String, Integer>(); // Stores keys with type `String` and values of type `Integer`
  
  myFriends.put("Mark", 24);
  myFriends.put("Cassie", 25);
  
  System.out.println(myFriends.get("Cassie")); // Prints out `25`
  
  System.out.println(myFriends.size()); // Number of key-value pairs
  
  for(String name: myFriends.keySet()){ // `keyset` returns list of keys
    System.out.println(name + " is age: " + myFriends.get(name));
  }
  
  ```
