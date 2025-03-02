### Exercises with Scanner 
Today's tasks should be coded using a text editor. For each task you will create a new folder and start by adding a class called <code>Main</code> (referred to as "The Main class" or the "client class" in the following).
This class will usually contain the <code>main</code> method (not so in Task 3). 

In Task 2 you will write all the code in the <code>main</code> method, while in 1 and 4 you will be asked to make 
both a <code>Main</code> class with a <code>main</code> method in it, and an "entity class" - a class representing a thing in the world
with a constructor and some fields/attributes/instance variable. 

NOTE: Task 5 is a continuation of Task 4. There are many small steps and you might loose track. Follow the steps as far as you can. Use the hints and codesnippets provided. The goal is to prepare yourself for review, where we will code it together. 

---
## Task 1:
In this exercise you will write an entity class called <code>Team</code> and a client class called <code>Main</code>. You will create private attributes in the entity class and give it a parameterized constructor, a <code>toString()</code> and a setter method.

1.a Create a class <code>Main</code> with a <code>main</code> method.

1.b Create an entity class called <code>Team</code>.

1.c Add a private instance variable/attribute to <code>Team</code> to hold the team's name.

1.d Add another private instance variable to hold the team's rank (some number).

1.e Add yet another private instance variable to hold the names of players in the team. 

1.f Add a constructor with a parameter, so that the <code>Team</code> can be instantiated with a team name. Make sure the parameter value is assigned to the mathcing instance variable in the constructor.
<details>
  <summary>Hint</summary>
  <p><code>public Team(String teamName)</code></p>
</details>

1.g In the <code>main</code> method in the <code>Main</code> class, create an instance of the <code>Team</code> class (i.e. instantiate the <code>Team</code> class).

1.h In the <code>Team</code> class add a method called <code>setRank()</code> that takes a number as parameter and assigns it to the rank attribute.

1.i From the <code>main</code> method, call the method <code>setRank()</code> on the instance of <code>Team</code> you created in step 1.g with a number of your choice.

1.j In the <code>Team</code> class add a <code>toString()</code> method that returns a String formated like this:

"Hold: De Uovervindelige
Rang: 3" 

(Precise wording will depend on the name and rank of the <code>Team</code> instance you created in step 1.g)

1.k From the <code>main</code> method, create 5 more <code>Team</code> instances and print them using their <code>toString()</code> method.

1.l Previously you created an <code>ArrayList</code> of team playernames as an attribute in the <code>Team</code> class. Now add a new method to the class, which adds a name to this list. Call the method <code>addPlayer()</code> and give it a suitable parameter. 

1.m Adjust the <code>toString()</code> method so that each playername is a part of the returned String - preferably with each name on it's own line.


## Task 2: Scanner basics: calculate years to retirement 
This task will require you to use the <code>Scanner</code> class to get some data from the user. You will then use one of the inputs in a simple calculation, that will tell the user how many years they have to work before they can retire.

2.a: create a <code>Main</code> class with a <code>main</code> method.

2.b: In the <code>main</code> method start by printing this message to the user: "Please type your name".

2.c: Create a <code>Scanner</code> object for reading from the command line (remember to import the <code>Scanner</code> class from the util library: <code>import java.util.Scanner; </code>)
<details>
  <summary>Hint</summary>
  <p><code>Scanner scanner = new Scanner(System.in);</code></p>
</details>
2.d: Declare a <code>String</code> variable <code>name</code> and assign to it whatever is returned from a call to scanner's <code>nextLine()</code> method.
<details>
  <summary>peep solution</summary>
  <p><code>String input =  scanner.nextLine();</code></p>
</details>

2.e: Print the name of the user in a greeting (i.e. "Hello \<name\>") followed by the message "Please type your age"

2.f: Declare another variable of type int  called <code>age</code> and assign to it the value returned by the <code>nextInt()</code> method of the <code>Scanner</code> object (reuse the <code>Scanner</code> object created in 2.c).

2.g: Print the value the user writes (the <code>age</code> variable) i.e. like this: "You are \<age\> years old".

2.h: Declare a third variable of type int. To this variable, assign the calculated number of years until the user can retire. You may assume retirement starts at age 67. Print the result (i.e. like this: "You have \<x\> years until retirement").

---

## Task 3: Complete the GuessANumber class
3.a Open the java file above called <code>GuessANumber.java</code> and complete the code. Follow the steps written as comments in the <code>makeAGuess()</code> method. Recursion is mentioned. This means that the method must call itself. If you are unsure how to use recursion, you may use another strategy.
<details>
  <summary>Not sure about recursion?</summary>
  <p><a href="https://www.geeksforgeeks.org/recursion-in-java/">Read about it here</a></p>
</details>
---

## Task 4. Textbased menu for a game
In this program the user is presented with a list of actions to choose from. There will be two classes. The class <code>GameMenu</code> represents the menu and the other class <code>Main</code> instantiates and uses the menu. 

The point of this excersise is 
1. learning how to separate the code into client class and entity class. 
2. learning how to work with <code>ArrayLists</code>

4.a Create an entity class called <code>GameMenu</code>.

4.b Add a private instance variable <code>actions</code> with the type ArrayList\<String\> to the class.

4.c Add a constructor with a parameter of the type <code>ArrayList</code> to the constructor. This is so that objects of the <code>GameMenu</code> class can be instantiated with a list of actions.(shown in step 4.f)  
4.d In the <code>GameMenu</code> contructor, assign the list received as an argument to the instance variable <code>actions</code>. 

4.e Create a client class, <code>Main</code> with a <code>main</code> method. (You will use this class to test the <code>GameMenu</code> class).

4.f In the <code>main</code> method create an <code>ArrayList\<String\></code> called <code>actions</code>. Don't forget to import the <code>ArrayList</code> class. 
Add the following <code>String</code> values to the <code>actions</code> list:
+ "1) Start game"
+ "2) Resume game"
+ "3) Pause game"
+ "4) End game"

<details>
  <summary>Tip for testing:</summary>
You can test the actions <code>ArrayList</code> by printing one of the elements:

<code>
System.out.print(actions.get(2)) // expected output: "Pause game"
</code>
</details>

4.g Still in the <code>main</code> method, instantiate the<code>GameMenu</code> class with the <code>actions</code> list as an argument to the constructor. 

4.h In the <code>GameMenu</code> class add a method <code>displayMenu()</code> that prints out the elements of the actions attribute. 
<details>
  <summary>Hint</summary>
  <p>you may use a <code>for-each</code>loop for printing the options
  </p>
</details>

4.i From the <code>main</code> method in <code>Main</code> test the <code>displayMenu()</code> method by calling it on the <code>GameMenu</code> instance created in step 4.g. 


## Task 5:
We will continue with the code you produced in Task 4. Now we want to make it possible for a user to select an action in the menu. When he types a number associated with an action, the program will print a message that corresponds to the chosen action. 
The point of this exercise is to work with the <code>Scanner</code> to create a dialog with the user.

5.a Create a method in the <code>GameMenu</code> class <code>getAction()</code> that prints the sentence "Type a number to choose an action" and then prints each elements in the <code>actions</code> attribute. 
 <details>
  <summary>Hint</summary>
  <p>Reuse the <code>displayMenu</code> method you wrote in step 4.h to accomplish the last bit. 
  </p>
</details>

5.b Next, in the <code>getAction()</code> method, create a new <code>Scanner</code> object. Declare a variable <code>String choice</code> and assign it the user's input. (Similar to what you did in step 2.c and 2.d).
5.c Let the <code>getAction()</code> method return the user's choice. (If the method has <code>void</code> as return type, change that to the return type <code>String</code>). Then return the choice variable you declared in step 5.b 

5.d In the <code>main</code> method of the <code>Main</code> class, call the <code>getAction()</code> method on the <code>GameMenu</code> instance you instantiated in 4.g, saving the return value (the user response) in a variable. 
<details>
  <summary>Peep solution</summary>
  <p>
    <code>
    String userChoice = getAction();
</code>
</p>
</details>

5.e Create a new method in the <code>Main</code> class for printing the message that corresponds to the action the user has chosen. The method should have this signature: <code>public static void doAction(int action)</code>. 

5.f In the body of the <code>doAction()</code> method, write a <code>switch-case</code> with a case for each of the 4 options added in step 4.f. In each case block you will print a message that corresponds to the user's choice:
   + 1: "Starting the game now"
   + 2: "Fetching previously saved game data"
   + 3: "Game paused"
   + 4: "Ending game"

5.g In step 5.d you created a variable called <code>userChoice</code> with the type <code>String</code>. Convert the value to an int before using it as an argument in a call to the <code>doAction()</code> method.
<details>
  <summary>Hint</summary>
  <p>
    You can parse from a <code>String</code> to an int by using
    <code>
    Integer.parseInt()
</code>
    Look it up in Java's API.
</p>
</details>





