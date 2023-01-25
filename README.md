# Variables

## Learning Goals

- Explain what a variable is in Java.
- Show how to initialize a variable.
- Discuss the naming convention when naming variables.

## Introduction

Consider our program we have been working with thus far:

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

As we have already discovered, this program will print out the phrase,
"Hello World". We can change what this program prints out by changing the
"Hello World" to something else, like this:

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("My name is Katie.");
    }
}
```

Now if we run this program in IntelliJ as we had before, instead of printing
out "Hello World", it will print "My name is Katie".

```text
My name is Katie.
```

But what if your name isn't Katie? We could change the entire phrase to be
"My name is <your name>". But there are a lot of names in this world. And we may
not always want to change this phrase every single time we encounter a new
person.

## What is a Variable?

A **variable** is a container in which we can store a value in. For example,
maybe we want to store the value of the name "Katie". To do that, we can write
the following:

```java
public class Main {
    public static void main(String[] args) {
        String name = "Katie";
    }
}
```

The first part of that statement is the type of variable, which indicates to
Java the kind of value we are expecting to store in this variable. The second
part is the name we want to be able to refer to the variable as. Once we define
a variable, we can give it a value, and we can refer to it at a later stage.

Now if we want to change the name, we can easily just change the name variable
rather than the whole phrase, like this:

```java
public class Main {
    public static void main(String[] args) {
        String name = "Katie";
        System.out.println("My name is:");
        System.out.println(name);
    }
}
```

Notice we can pass the `name` variable right into the `println()`! If we run
this program now, it'll print the following:

```text
My name is:
Katie
```

Try changing the `name` variable to your name now! Then run the program and see
if it prints out your name!

We can even change the value of the variable later on too! Modify the program to
look like this:

```java
public class Main {
    public static void main(String[] args) {
        String name = "Katie";
        System.out.println(name);
        
        // Change the variable's value
        name = "Emily";
        System.out.println(name);
    }
}
```

Notice halfway through the program, we change the value of `name`. What do you
think the program will output now?

<details>
    <summary>What do you think the program will output now?</summary>

  <p>Answer: <br>
     <p><code>Katie</code></p>
     <p style="margin-top: -18px"><code>Emily</code></p>
  </p>

</details>

We could also initialize the variable after defining it like this:

```java
public class Main {
    public static void main(String[] args) {
        String name;
        name = "Katie";
        System.out.println(name);
    }
}
```

In this case, it would make more sense for us to just initialize the variable to
the value, "Katie", but this is just another possibility for demonstration
purposes.

## Variable Naming Convention

By convention, in Java the name of the variable usually starts with a lowercase
character.

- If the name of the variable has multiple words in it, the first word will start
  with a lowercase character and every word after will start with an uppercase
  character. For example: `bikeColor`.
  - This is often referred to as "**camel case**".
- There are some exceptions to this style guide, but we will cover them as they
  come up.
