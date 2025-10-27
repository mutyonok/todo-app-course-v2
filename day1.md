## **Day 1 Tasks — Data and Functions**

### **Task 1 – Create a place to store tasks**

**Goal:**

You need a single global variable to hold all tasks.

**Instructions:**

* Think of this variable as a box where you’ll keep all your todo items.
* The box should start empty.
* The variable should be accessible from any function in your program, because many functions will need to read from and write to it later.

**Concept Explanation:**

- A *global variable* is one that lives outside any function so that all functions in your script can see and update it.
- An *array* is a list-like structure that can store multiple values—in our case, each task object.

### Debugging Checks

* After declaring your global variable, open the console and type its name — it should show `[]`.
* Make sure you can still see and access it from inside a function (log it inside a test function).
* If you get “undefined” or an error like “not defined,” confirm that your variable is declared outside any function block.

**If stuck, search / ask AI:**

* Search: “javascript create empty array global variable”
* Ask AI: “Explain how to make a global array variable in JavaScript and why it’s accessible from functions”

---

### **Task 2 – Add new tasks to the list**

**Goal:**

Create a function that can take a piece of text and add a new task to your list.

**Instructions:**

* The function should receive the task text as input.
* Inside the function, create a new task object that has two properties:
  * one for the task’s text
  * one for whether it’s completed (start with false)
* Add this new task object to your global list of tasks.
* Think of this as “writing something new into your notebook.”

**Concept Explanation:**

- A *function* groups reusable actions.
- A *parameter* lets you pass data into a function.
- An *object* stores related pieces of data together using property names.
- The *array push()* method adds a new item to the end of an array.

### Debugging Checks

* Add a `console.log()` inside your function to show:

  * The text received as the parameter.
  * The task object just before it’s added to the array.
* After calling the function, check the global array in the console — it should now contain one more item.
* If nothing changes, check for typos in the array name or confirm that `.push()` is being called on the correct variable.
* If `completed` isn’t showing up, verify the object uses the right property names.


**If stuck, search / ask AI:**

* Search: “javascript add object to array using push”
* Ask AI: “Show how to create a function that takes a parameter and adds an object to an array in JavaScript”

---

### **Task 3 – Show all tasks in the console**

**Goal:**

Write a function that goes through your list and shows every task’s text and completion status.

**Instructions:**

* The function should look at every task currently stored in your list.
* For each task, print out both pieces of information: what the task says, and whether it’s completed or not.
* This will let you check that your add-function worked correctly.

**Concept Explanation:**
A *loop* lets you repeat an action for each item in an array.
The *console.log()* function displays information in the browser’s developer console so you can inspect your program’s state.

### Debugging Checks

* Add a `console.log()` at the start of the printing function to confirm it’s being called.
* Inside the loop, log the current index or task to see the function iterating correctly.
* If nothing prints, check that the function name in your call matches the definition.
* If it prints `undefined`, check how you’re accessing task properties — they should match the object’s keys.
* If the loop never runs, ensure the array isn’t empty (call `console.log(tasks.length)` to confirm).


**If stuck, search / ask AI:**

* Search: “javascript loop through array and log each object property”
* Ask AI: “Explain how to loop through an array of objects and print each property in JavaScript”

---

### **Testing Scenario**

1. Open your browser console.
2. Type the name of your global tasks variable and press enter. There should be no errors and the result should be empty array.
3. Add several tasks using your “add” function.
4. Call your “print” function and confirm that all tasks appear with the right text and completion status.
