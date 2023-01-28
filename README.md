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
part is the name we want to be able to refer to the variable as. Once we declare
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

## Terminology

Let's go over a couple of terms you may hear: declaring, initializing, and
assigning.

**Declaring**: A variable declaration is when we introduce a variable into
a program. We declare a variable like this:

```java
// The variable, name, is declared
String name;
```

Notice when we declare a variable, we must put the data type in front of the
variable name, as this is how we define a variable.

**Initializing**: A variable initialization is when we give or assign an initial
value to a variable. We can initialize a variable like this:

```java
// The variable, name1, is declared AND initialized to "Katie"
String name1 = "Katie";

// The variable, name2, is declared
String name2;

// The variable, name2, is now initialized to "Emily"
name2 = "Emily";
```

When we declare and initialize a variable at the same time, we must put the data
type in front of the variable name to first declare the variable.

If we initialize after, we do not need to put the data type in front of the
variable name as it has already been declared.

**Assigning**: A variable assignment or re-assignment occurs when we provide a
value to a variable. We can assign a variable like this:

```java
// The variable, name, is declared
String name;

/* The variable is now being initialized AND assigned to "Katie"
   Note: Initialization is referred to the first time a variable is assigned a value */     
name = "Katie";

// The variable is now being assigned (or re-assigned) to "Emily"
name = "Emily";
```

It is important to note that in order to use the variable, it must be
initialized to a value prior to trying to use it in a statement. Let's look at
what happens when we declare a variable, but don't initialize it and try to use
it.

IntelliJ will first warn us of an error:

![use-variable-without-initialization-intellij](https://curriculum-content.s3.amazonaws.com/java-mod-1/variables/intellij-use-variable-without-initialization.png)

If we ignore the error and still try to run the program, the compiler will then
throw the following error:

```text
java: variable name might not have been initialized
```

We cannot use a variable that has not been initialized because we have not
assigned it an initial value yet.

## Comprehension Check

Consider the following code:

```java
public class Main {
    public static void main(String[] args) {
        String name;
        name = "Katie";
        System.out.println(name);
    }
}
```

<details>
    <summary>What do you think the program will output?</summary>

  <p>Answer: <br>
     <p><code>Katie</code></p>
  </p>

  <p>Even though the variable, <code>name</code>, is declared on a different line from where it is initialized, it will still assign the <code>name</code> variable to "Katie".</p>
  <p>In this case, it would make more sense for us to just initialize the variable to the value, "Katie", but this is just another possibility for demonstration purposes.</p>

</details>

Let's modify the code a little bit. Consider the modified program:

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

<details>
    <summary>What do you think the program will output now?</summary>

  <p>Answer: <br>
     <p><code>Katie</code></p>
     <p style="margin-top: -18px"><code>Emily</code></p>
  </p>

  <p>We re-assign the variable <code>name</code> to "Emily" halfway through the program. Therefore, when we do that, if we print out the <code>name</code>variable again, it will now print the re-assigned value.</p>

</details>

## Variable Naming Convention

By convention, in Java the name of the variable usually starts with a lowercase
character.

- If the name of the variable has multiple words in it, the first word will start
  with a lowercase character and every word after will start with an uppercase
  character. For example: `bikeColor`.
  - This is often referred to as "**camel case**".
- There are some exceptions to this style guide, but we will cover them as they
  come up.
