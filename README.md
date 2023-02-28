### Exercises with Scanner 
Today's tasks should be coded using a text editor. For each Task you will create a new folder and start by adding a Main class with a main method (except for Task 2). 
In task 2 you will write all the code in this main method, while in 1 and 4 you will be asked to make both a Main class with a main method in it (sometimes refered to as the "client class") and an "entity class" whithout a main method but with a constructor. 

NOTE: Task 5 is a continuation of Task 4. There are many small steps and you might loose track. Follow the steps as far as you can. Use the hints and codesnippets provided. The goal is to prepare yourself for review, where we will code it together. 

---
## Task 1:
In this exercise you will code an entity class Team and a client class Main. You will create private attributes on the entity class and give it a parameterized constructor, a toString and a setter method.

1.a Create a class Main with a main method.

1.b Create an entity class called Team.

1.c Add a private instance variable a.k.a attribute to Team to hold the team name.

1.d Add another private instance variable to hold the Teams rank (some number).

1.e Add yet another private instance variable to hold the names of players in the team. 

1.f Add a constructor with a parameter, so that the Team can be instantiated with a team name. Make sure the parameter value is assigned to the mathcing instance variable.
<details>
  <summary>Hint</summary>
  <p><code>public Team(String teamName)</code></p>
</details>

1.g From the main method in the Main class, create an instance of the Team class (instantiate the Team class).

1.h In the Team class add a method called <code>setRank</code> that takes a number and assigns it to the rank attribute.

1.i From the main method, call the method setRank on the instance of Team you created in step 1.g with a number of your choice.

1.j In the Team class add a <code>toString</code> method that returns a String formated like this:

"Hold: De Uovervindelige
Rang: 3" 

(Precise wording will depend on the name and rank of the Team instance you have created in step 1.g)

1.k From the main method, create 5 more Team instances and print them.


## Task 2: Scanner basics: calculate years to retirement 
This task will require you to use the Scanner type, to get some data from the user. You will then use one of the inputs in a simple calculation, that will tell the user how many years they have to work before they can retire.

2.a: create a Main class with a main method.

2.b: In the main method start by printing a message to the user: "Please type your name".

2.c: Create a Scanner object for reading the command line (remember to import the Scanner class from the util library: <code>import java.util.Scanner; </code>)
<details>
  <summary>Hint</summary>
  <p><code>Scanner scanner = new Scanner(System.in);</code></p>
</details>
2.d: Declare a String variable, <code>name</code> and assign the content of the scanners call to <code>nextLine() to it.</code>
<details>
  <summary>peep solution</summary>
  <p><code>String input =  scanner.nextLine();</code></p>
</details>

2.e: Print the name of the user in a greeting, followed by the message "Please type your age"

2.f: Declare another variable of type int, <code>age</code> and assign it the value returned by the nextInt method of the Scanner object. (you may reuse the Scanner object created in 2.c).

2.g: Print the value the user writes (print the <code>age</code> variable)

2.h: Declare a third variable of type int. To this variable, assign the calculated number of years until the user can retire. You may assume retirement starts at 67 years. Print the result.

---

## Task 3: Finish the GuessANumber class
3.a Open the java file above called GuessANumber.java and try to finish the code. Follow the steps written as comments in the <code>makeAGuess</code> method. Recursion is mentioned. This means that the method must call itself.
<details>
  <summary>Not sure about recursion?</summary>
  <p><a href="https://www.geeksforgeeks.org/recursion-in-java/">Read about it here</a></p>
</details>
---

## Task 4. Textbased menu for a game
In this program the user is presented with a list of actions. There will be two classes. One, GameMenu represents the menu and the other, Main, instantiates and uses the menu. 

The point of this excersise is 
1. learning how to separate the code into client class and entity class. 
2. learning how to work with ArrayLists


4.a Create an entity class, GameMenu.

4.b Add a private instance variable, <code>actions</code> of type ArrayList\<String\> to the class.

4.c Add a constructor with a parameter of type ArrayList. This is so that the GameMenu class can be instantiated with a list of actions.(shown in step 4.f)  
4.d In the GameMenu contructor, assign the list received as an argument, to the instance variable <code>actions</code>. 

4.e Create a client class, Main with a main method. (You will use this class to test the GameMenu class) after the next step.

4.f In the main method create an ArrayList of type String called <code>actions</code>. Don't forget to import the ArrayList class. 
Add the following String values to the <code>actions</code> ArrayList:
+ "1) Start game"
+ "2) Resume game"
+ "3) Pause game"
+ "4) End game"

<details>
  <summary>Tip for testing:</summary>
You can test the actions ArrayList by printing one of the elements:

<code>
System.out.print(actions.get(2)) // expected output: "Pause game"
</code>
</details>

4.g Still in the main method, instantiate the GameMenu class with the actions reference as an argument to the constructor. 

4.h In the GameMenu class add a method <code>displayMenu</code> that prints out the elements of the actions attribute. 
<details>
  <summary>Hint</summary>
  <p>you may use a <code>for-each</code>loop for printing the options
  </p>
</details>

4.i From the main method in Main, test the displayMenu method by calling it on the GameMenu instance created in step 4.g. 


## Task 5:
We will continue with the code you produced in task 4. Now we want to make it possible for a user to select an action in the menu. When he types a number associated with an action, the program will print a message that corresponds to the chosen action. 
The point of this exercise is to work with the Scanner to create a dialog with the user.

5.a Create a method in the GameMenu class, <code>getAction</code> that prints the sentence "Type a number to choose an action" and then prints each elements in the <code>options</code> attribute. 
 <details>
  <summary>Hint</summary>
  <p>Reuse the displayMenu method you wrote in step 4.h to accomplish the last bit. 
  </p>
</details>

5.b Next, in the <code>getAction</code> method, create a new Scanner object. Declare a variable <code>String choice</code> and assign it the user's input. (Similar to what you did in step 2.c and 2.d)

5.c Let the <code>getAction</code> method return the user's choice. (If the method has void as return type, change that to the return type of String). Then return the choice variable you declared in step 5.b 

5.d In the main method of Main, call the <code>getAction</code> method on the Menu instance, saving the return value (the user response) in a variable. 
<details>
  <summary>Peep solution</summary>
  <p>
    <code>
    String userChoice = getAction();
</code>
</p>
</details>

5.d Create a new method in the Main class, for printing the message that corresponds to the action the user has chosen. The method should have this signature: <code>public static void doAction(int action)</code>. 

5.f In the body of the <code>doAction</code> method, write a <code>switch-case</code> with a case for each of the 4 options added in step 4.f. In each case block you will print a message that corresponds to the user's choice:
   + 1: "Starting the game now"
   + 2: "Fetching previously saved game data"
   + 3: "Game paused"
   + 4: "Ending game"

5.g In step 5.d you created a variable called <code>userChoice</code>code> of type String. Convert the value to an int before using it as an argument in a call to the <code>doAction</code> method.
<details>
  <summary>hint</summary>
  <p>
    <code>
    Integer.parseInt()
</code>
</p>
</details>





