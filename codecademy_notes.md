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




