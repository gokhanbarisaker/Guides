# Basics #

[A test is not a unit test](http://www.artima.com/weblogs/viewpost.jsp?thread=126923) if:

* It talks to the database
* It communicates across the network
* It touches the file system
* It can't run at the same time as any of your other unit tests
* You have to do special things to your environment (such as editing config files) to run it.


## Dependencies ##

* JUnit 4.12
* Hamcrest 1.3


## Nomenclature ##

### Test classes ###

For each class, there should be a test class with `Test` suffix.

Class | Test class
------|-----------
Foo   | FooTest


### Test methods ###

Follow the auto generated test case naming rule. For each method, there should be a test method with `test` prefix.

Method | Test method
-------|------------
bar    | testBar

Decoupling expected behaviors by adding `expected behaviour` as a suffix might be a great flavor.

Expected behavior | Method | Test method
------------------|--------|---------------
Success           | bar    | testBarSuccess
Failure           | bar    | testBarFailure


## Test case ##

```java
public class Foo {
  @Test
  public void testBar() {
    // Arrange,
    // Act,
    // Assert,
    // Move on...
  }
}
```

## Usage ##

* [Arrange](./arrange.junit)
* [Act](./act.junit)
* [Assert](./assert.junit)
