# JavaSE-Nested Clases

See the Udemy course: https://www.udemy.com/course/curso-certificacion-profesional-desarrollador-java-se-11

In Java, a nested class is a class defined within another class. 

There are four types of nested classes in Java: static nested classes, non-static nested classes (inner classes), local classes, and anonymous classes. 

Let me give you examples of each:

## 1. Static Nested Class:
```java
class OuterClass {
    // ...

    static class StaticNestedClass {
        void display() {
            System.out.println("This is a static nested class.");
        }
    }
}
```

To instantiate the static nested class:

```java
OuterClass.StaticNestedClass nestedObject = new OuterClass.StaticNestedClass();
nestedObject.display();
```

## 2. Non-static Nested Class (Inner Class):

```java
class OuterClass {
    // ...

    class InnerClass {
        void display() {
            System.out.println("This is an inner class.");
        }
    }
}
```

To instantiate the inner class:

```java
OuterClass outerObject = new OuterClass();
OuterClass.InnerClass innerObject = outerObject.new InnerClass();
innerObject.display();
```

## 3. Local Class:

Local classes are defined within a block of code, typically within a method.

```java
cass OuterClass {
    // ...

    void someMethod() {
        class LocalClass {
            void display() {
                System.out.println("This is a local class.");
            }
        }

        LocalClass localObject = new LocalClass();
        localObject.display();
    }
}
```

## 4. Anonymous Class:

Anonymous classes are used for creating an instance of a class and implementing its interface at the same time.

```java
interface MyInterface {
    void myMethod();
}

class OuterClass {
    void createAnonymousClass() {
        MyInterface anonymousObject = new MyInterface() {
            @Override
            public void myMethod() {
                System.out.println("Anonymous class implementing MyInterface");
            }
        };

        anonymousObject.myMethod();
    }
}
```

These are the basic examples of each type of nested class in Java. 

Each type has its use cases, and the choice depends on the specific requirements of your program.
