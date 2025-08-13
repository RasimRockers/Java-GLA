In Java, **`Scanner`** is a class in the `java.util` package used to take **input** from various sources, most commonly from the **keyboard**.

**Key points:**

* You need to **import** it:

  ```java
  import java.util.Scanner;
  ```
* It can read different data types: `int`, `double`, `String`, `boolean`, etc.
* It reads input **token by token** (split by whitespace) unless you use special methods like `nextLine()`.

**Example:**

```java
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);  // Create Scanner object
        
        System.out.print("Enter your name: ");
        String name = sc.nextLine();  // Read a line of text
        
        System.out.print("Enter your age: ");
        int age = sc.nextInt();       // Read an integer
        
        System.out.println("Hello " + name + ", you are " + age + " years old.");
        
        sc.close();  // Close scanner to prevent resource leaks
    }
}
```

**Common methods of `Scanner`:**

| Method          | Description                             |
| --------------- | --------------------------------------- |
| `nextInt()`     | Reads an integer                        |
| `nextDouble()`  | Reads a double                          |
| `next()`        | Reads a single word (until space)       |
| `nextLine()`    | Reads the whole line (including spaces) |
| `nextBoolean()` | Reads a boolean value (true/false)      |

