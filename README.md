# Sample Maven Project

This is a simple Java project using Maven, designed for basic CI/CD pipelines and tools such as **UrbanCode Build**. It builds a JAR file containing a basic `HelloWorld` class and a JUnit test.

---

## 🛠 Project Structure

sample-maven-project/
├── pom.xml
├── src/
│ ├── main/
│ │ └── java/
│ │ └── com/example/HelloWorld.java
│ └── test/
│ └── java/
│ └── com/example/HelloWorldTest.java

yaml
Copy
Edit

---

## 🚀 How to Build

Make sure you have [Maven](https://maven.apache.org/) installed and available in your `PATH`.

```bash
mvn clean package
The output JAR will be located at:

bash
Copy
Edit
target/sample-maven-project-1.0.0.jar
▶️ How to Run
After building:

bash
Copy
Edit
java -jar target/sample-maven-project-1.0.0.jar
Expected output:

csharp
Copy
Edit
Hello from Maven + UrbanCode Build!
🧪 Run Tests
bash
Copy
Edit
mvn test
You should see:

yaml
Copy
Edit
Running com.example.HelloWorldTest
Hello from Maven + UrbanCode Build!
Tests run: 1, Failures: 0, Errors: 0, Skipped: 0
🧩 Integration with UrbanCode Build
To use this in IBM UrbanCode Build:

Point your SCM configuration to this repository

Use Maven plugin with clean package as the goal

Optional: use versions:set to update the version via buildlife

📦 Dependencies
Java 8+

Maven 3+

JUnit 4.13.2

📄 License
This project is open-source and available for educational or demo purposes.

arduino
Copy
Edit

---

## 🧪 `src/test/java/com/example/HelloWorldTest.java`

```java
package com.example;

import org.junit.Test;

public class HelloWorldTest {

    @Test
    public void testMainMethodRuns() {
        // This test ensures the main method runs without error
        HelloWorld.main(new String[]{});
    }
}
🖥️ src/main/java/com/example/HelloWorld.java
java
Copy
Edit
package com.example;

public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello from Maven + UrbanCode Build!");
    }
}
