# Interview

--- 

### Question 1

What will be the output of this code ?

~~~~
public enum Day {
	SUNDAY, MONDAY, TUESDAY, WEDNESDAY, 
	THURSDAY, FRIDAY, SATURDAY
}

public class Test {
	Set mySet = new TreeSet();
	mySet.add(Day.MONDAY);
	mySet.add(Day.SUNDAY);
	mySet.add(Day.SATURDAY);

	for(Day d: mySet){
		System.out.println(d);
	}
}
~~~~

---
### Question 2

Identify the problem in the below code:

~~~~
public class Foo {
    public Foo() {
        doSomething();
    }

    public void doSomething() {
        System.out.println("do something acceptable");
    }
}

public class Bar extends Foo {
    public void doSomething() {
        System.out.println("yolo");
        Zoom zoom = new Zoom(this); 
    }
}
~~~~

---

### Question 3

int a = 1L; Won’t compile and int b = 0; b += 1L; compiles fine. Why ?

---

### Question 4

~~~~
public class Test
{
    public static void main(String[] args)
    {
        Integer a = 1000, b = 1000;
        System.out.println(a == b);

        Integer c = 100, d = 100;
        System.out.println(c == d);
    }
}
~~~~

+++

outputs:

~~~~
false
true
~~~~

Why is the code printing true in the second and false in the first case?

---
### Question 5

What is the problem with this code:

~~~~
final byte[] bytes = someString.getBytes();
~~~~

---

### Question 6

What is the problem with this code?

~~~~
final Path path = Paths.get(...);

Files.lines(path).forEach(System.out::println);
~~~~

---

### Question 7

Consider the following piece of code:

~~~~
final List<Integer> list = new ArrayList<>();

list.add(1);
list.add(2);
list.add(3);

list.remove(2);
~~~~

What will be the contents of the list after this operation and why?

---

### Question 8

Describe and compare fail-fast and fail-safe iterators. Give examples.

---

### Question 9

What does the following Java program print?

~~~~
public class Test {
    public static void main(String[] args) {
        System.out.println(Math.min(Double.MIN_VALUE, 0.0d));
    }
}
~~~~