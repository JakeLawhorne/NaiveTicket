# NaiveTicket

The second Objects lab, from the BlueJ book's second chapter.

First you need to FORK this repo into your account, then you need to CLONE that foreked repo, the one in your account. 
When you are finished with your code, be sure to ADD/COMMIT and PUSH your code to your repo.

Use the URL from your repo as the submission to the portal. 

Look for the [Chapter 2 file](./doc/BlueJ-objects-first-ch2.pdf) you need in the [doc](./doc) folder.
There is 35 pages of reading and exercises in the chapter.

Work through all these exercises. You edit this file with your answers for these exercises.

### Exercise 2.1
* Create a TicketMachine object on the object bench.
* Upon viewing its methods, `getBalance`, `getPrice`, `insertMoney`, `printTicket`.
* Use `getPrice` method to view the value of the price of the tickets that was set when this object was created.
* Use `insertMoney` method to simulate inserting an amount of money into the machine.
* Use `getBalance` to check that the machine has a record of the amount inserted.
    * You can insert several separate amounts of money into the machine, just like you might insert multiple coins or notes into a real machine. Try inserting the exact amount required for a ticket. As this is a simple machine, a ticket will not be issued automatically, so once you have inserted enough money, call the `printTicket` method. A facsimile ticket should be printed in the BlueJ terminal window.

### Exercise 2.2
* What value is returned if you check the machine’s balance after it has printed a ticket?
    0
### Exercise 2.3
* Experiment with inserting different amounts of money before printing tickets.
    * Do you notice anything strange about the machine’s behavior?
        The balance increases corresponding to the amount inserted.
    * What happens if you insert too much money into the machine – do you receive any refund?
        No, you don't get a refund. you receive a ticket, then the balance is set to 0.
    * What happens if you do not insert enough and then try to print a ticket?
        It still prints the ticket, and the balance is increased substantially (weird)

### Exercise 2.4
* Try to obtain a good understanding of a ticket machine’s behavior by interacting with it on the object bench before we start looking at how the `TicketMachine` class is implemented in the next section.

### Exercise 2.5
* Create another ticket machine for tickets of a different price.
    * Buy a ticket from that machine.
    * Does the printed ticket look different?
    The ticket price is changed in the string
### Exercise 2.6
* Write out what you think the outer wrappers of the `Student` and `LabClass` classes might look like – do not worry about the inner part.
public class Student{
    
}

public class Lab Class{
    
}

### Exercise 2.7
Does it matter whether we write<br>
`public class TicketMachine`<br>
or<br>
`class public TicketMachine`<br>
in the outer wrapper of a class?

* Edit the source of the `TicketMachine` class to make the change and then close the editor window.
    * Do you notice a change in the class diagram?
        - there are red boxes on the left side of the file
    * What error message do you get when you now press the compile button?
        - <identifier expected>
        - class, interface, enum, or record expected
    * Do you think this message clearly explains what is wrong?
        -well, it's expecting a class, and we're giving it incorrectly.

### Exercise 2.8
* Check whether or not it is possible to leave out the word `public` from the outer wrapper of the `TicketMachine` class.
    Apparently I can still make a ticket machine, but the tickettest is posting an error (that is not named). Im wondering that the functionality is sound, it's just that because it's not public the test cannot access it.
### Exercise 2.9
* From your earlier experimentation with the ticket machine objects within BlueJ you can probably remember the names of some of the methods – `printTicket`, for instance.
    * Look at the class definition in Code 2.1 and use this knowledge, along with the additional information about ordering we have given you, to try to make a list of the names of the fields, constructors, and methods in the `TicketMachine` class.
    * Hint: There is only one constructor in the class.
    
    -Fields: price, balance, total, ticket number
    -Constructors: public TicketMachine(Integer ticketCost)
    -Methods: getPrice(), getTicketNumber(), getBalance(), insertMoney(Integer amount), calculateTotal(), incrementTicketNumber(),printTicket()

### Exercise 2.10
* Do you notice any features of the constructor that make it significantly different from the other methods of the class?
    It has a parameter, and it has attributes being given to the object
### Exercise 2.11
* What do you think is the type of each of the following fields?
    

```java
private int count; ---> int
private Student representative; ---> Student
private Server host; ---> Server
```

### Exercise 2.12
* What are the names of the following fields?

```java
private boolean alive; --> alive
private Person tutor; ---> tutor
private Game game; ---> game
```
### Exercise 2.13

In the following field declaration from the TicketMachine class<br>

```java
private int price;
```
does it matter which order the three words appear in? Yes
* Edit the `TicketMachine` class to try different orderings. After each change, close the editor.
    * Does the appearance of the class diagram after each change give you a clue as to whether or not other orderings are
possible? Yes, it gives you red error boxes on the left
    * Check by pressing the compile button to see if there is an error message. <missing Identifier>
    * Make sure that you reinstantiate the original version after your experiments!

### Exercise 2.14
* Is it always necessary to have a semicolon at the end of a field declaration? Yes
* Once again, experiment via the editor.
* The rule you will learn here is an important one, so be sure to remember it.


### Exercise 2.15
* Write in full the declaration for a field of type `int` whose name is `status`.

int status;

### Exercise 2.16
* To what class does the following constructor belong?
```
public Student(String name)

Student
```

### Exercise 2.17
* How many parameters does the following constructor have and what are their types?
```
public Book(String title, double price)

2, string, double
```

### Exercise 2.18
* Can you guess what types some of the `Book` class’s fields might be? strings, chars, integers, float
* Can you assume anything about the names of its fields? string paragraph, int pagecount, string chapter, float chaptersection

READ upto and INCLUDING section 2.15 of this chapter.

2.2 Price is null

2.21 The names of the methods and return names are different
2.22 The amount of money inserted into the machine
2.23 No it works
2.25 will not compile
2.26 type string vs type int; all getTotal does is return the total value, the printString method is:running the increment ticket number method, performs addition arithmetic operation on the total field, clears the balance, and then prints the ticket cost and the total amount that was collected by the machine.
2.27 Yes. When i remove return statements from either method they fail to compile and will not work.
2.29 Constructors do not have return types
2.35 Different outputs. I have the price set to the ticket cost parameter in the constructor. So, once the objects price is set as the ticket price, then when i call the price field in the show price method, it prints the same value.
2.36It would just print "# price cents" --> price is now a string literal and not a field value
2.37 It would print the same thing as 2.36
2.38 No because they aren't using the price value
2.39
