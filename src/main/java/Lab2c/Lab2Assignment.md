## Name: SID: Hidden for the public repository

### Part 1: Book.java

```java
package Lab2b;
public class Book {
private String chapters[];
private static final int DEFAULT_CHAPTERS = 10;    public Book() {
        chapters = new String[DEFAULT_CHAPTERS];
        for (int i = 0; i < chapters.length; i++) {
            chapters[i] = "n/a";
        }
    }    public Book(String argument[]) {
        chapters = new String[argument.length];
        for (int i = 0; i < argument.length; i++) {
            chapters[i] = argument[i];
        }
    }    public String getChapter(int i) {
        return chapters[i];
    }    public String[] getChapters() {
        return chapters;
    }
}

```

### Part 2: MobileComputer.Java

```java
package Lab2c;

public class MobileComputer extends Computer implements Chargeable {
  private int battery;

  public MobileComputer() {
    secret = "MobileComputer secret";
    battery = 5;
  }

  @Override
  public void work() {
    if (battery > 0) {
      System.out.println("It is working on my lap.");
      battery--;
    } else {
      System.out.println("Running out of battery.");
    }
  }

  public void charge() {
    if (battery < 10) {
      battery++;
    }
  }
}

```

> We add `implements Chargeable` into the MobileComputer
> ` public class MobileComputer extends Computer implements Chargeable`
> such that we can use and implement the methods provided by charger interface.
