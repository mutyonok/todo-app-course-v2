## **Day 2 — User Input: Connecting UI to Data**
### **Task 0 – Recall from Day 1: Data and Functions**

**Description:**
You already have a data model for tasks and basic functions that work with it. This review ensures everything still runs correctly before connecting it to the interface.

**Instructions:**

1. Re-read your code and find:
   * a global array for tasks,
   * a function that adds a new task to the array,
   * a function that prints all tasks to the console.
2. Explain out loud what each function does line by line.
3. In the browser console, manually call your functions:
   * Add a few tasks using your function that accepts text.
   * Print all tasks using your function that loops through them.
4. Confirm the output looks as expected (an array of task objects).

### **Task 1 – Create an input field and a button in HTML**

**Description:**
You’ll add a simple form where the user can type a new task and click a button to add it. This will be the visible way to add tasks to your list.

**Instructions:**

* In your HTML file, add one text input where users can type a task name.
* Add a button next to it labelled “Add Task.”

**Concept Explanation:**
HTML elements like `<input>` and `<button>` create interactive parts of a webpage.
The `type="text"` attribute makes a field where users can type.
Buttons can trigger JavaScript code when clicked.

**How to Test:**

1. Open your HTML file in the browser.
2. You should see a text box and a button labelled “Add Task.”
3. Try typing text into the input — make sure it accepts it.

**Debugging Hints:**

* If you see nothing on the page, make sure the HTML file is saved and reloaded.
* If the button appears but input doesn’t, check that you closed your tags correctly.
* If the text box is too small or missing, confirm `type="text"` is used.

**If stuck, search / ask AI:**

* Search: “HTML how to create a text input and button”
* Ask AI: “Show an example of HTML with a text input and a button next to it”


### **Task 2 – Access input and button elements in JavaScript**

**Description:**
You’ll write JavaScript to “find” your HTML elements so your code can read the input and respond to button clicks.

**Instructions:**

* In your JavaScript file, create a new variable outside of any functions and store the reference to the input element.
* Do the same for the button.
* You’ll use these variables in later tasks to get user input and react to clicks.

**Concept Explanation:**
JavaScript can access HTML elements through the *Document Object Model (DOM)*.
`document.querySelector()` lets you locate an element by its tag, class, or id so you can read or change it later.

**How to Test:**

1. Open the console.
2. Log both variables — they should show as HTML elements (e.g., `<input>` and `<button>`).
3. If either logs as `null`, the element wasn’t found.

**Debugging Hints:**

* If you get `null`, check that the selector matches your HTML exactly (for example, same id or tag).
* If you see “not defined,” check that your `<script>` tag is correctly linked and appears after the HTML elements in the body.
* Refresh after saving both HTML and JS files.

**If stuck, search / ask AI:**

* Search: “javascript querySelector example to get input and button”
* Ask AI: “Explain how to use document.querySelector in JavaScript to access HTML elements”

### **Task 3 – Handle button clicks with an event listener**

**Description:**
Now you’ll make the button interactive: when clicked, your code will run a function.

**Instructions:**

* Add an event listener to the button for the “click” event.
* When the button is clicked, log a simple message to the console (e.g., “Button clicked”).
* This confirms the connection between your HTML and JavaScript.

**Concept Explanation:**
Events are actions that happen in the browser (like clicks, key presses, etc.).
An *event listener* tells the browser to run specific code when an event occurs.
This is how web apps react to user interaction.

**How to Test:**

1. Open the page in the browser and open the console.
2. Click the button — your message should appear in the console every time you click.
3. Try multiple clicks to see the message repeat.

**Debugging Hints:**

* If nothing prints, check that your event listener is attached to the right element.
* If you get an error about `addEventListener`, confirm the variable actually holds the button element (log it first).
* Make sure your script is running *after* the HTML loads (script tag at bottom of body).

**If stuck, search / ask AI:**

* Search: “javascript addEventListener click button example”
* Ask AI: “How do I make JavaScript run a function when a button is clicked?”

### **Task 4 – Get text from the input field when the button is clicked**

**Description:**
You’ll now make the app actually read what the user typed in the input box when the button is pressed.

**Instructions:**

* Inside the event listener, access the input’s current text value.
* Log that text to the console to confirm it’s captured.
* (Later, you’ll use this value with your `addTask` function from Day 1.)

**Concept Explanation:**
HTML input elements store what the user types in the `value` property.
By reading `input.value`, you get the current text entered by the user.

**How to Test:**

1. Type something into the input.
2. Click the button.
3. You should see exactly what you typed appear in the console.
4. Try again with different text — each click should show the new value.

**Debugging Hints:**

* If the console shows an empty string, confirm you’re reading `input.value` *inside* the click event.
* If you get “undefined,” check that your variable name matches the one storing the input element.
* Refresh the page after saving.

**If stuck, search / ask AI:**

* Search: “javascript get value from input field on button click”
* Ask AI: “How do I read the text from an input field when a button is clicked in JavaScript?”

### **Task 5 – Clear the input field after clicking the button**

**Description:**
After adding a task, you want the input box to be empty again so users can type the next one easily.

**Instructions:**

* Inside your event listener, after reading the value, reset the input’s value to an empty string.
* Test that it clears visually after clicking the button.

**Concept Explanation:**
You can change an input’s content by setting its `value` property.
This is a simple example of updating the DOM to reflect a new state.

**How to Test:**

1. Type any text in the box.
2. Click the button.
3. You should see the console log your text and the input field should immediately clear.
4. Try typing again — it should always clear after clicking.

**Debugging Hints:**

* If it doesn’t clear, make sure you’re setting `input.value` *after* reading it.
* If it clears before logging, check the order of operations in your code.
* Ensure there are no typos in the variable names.

**If stuck, search / ask AI:**

* Search: “javascript clear input field after button click”
* Ask AI: “Explain how to reset a text input value in JavaScript after using it”

### **Task 6 – Connect input with your addTask and printTasks functions**

**Description:**
You’ll now connect your Day 1 code with your UI. The user’s typed text should become a new task in your data list.

**Instructions:**

* Inside the event listener, call your existing `addTask()` function using the input value.
* Then call your `printTasks()` function to show the updated list in the console.
* Finally, clear the input as before.

**Concept Explanation:**
This is where your app becomes *data-driven*: user actions (clicks) trigger functions that modify data and then display results.
Each function now works together — input (UI) → add task (data) → print tasks (feedback).

**How to Test:**

1. Type a task and click the button.
2. Open the console — you should see your task list printed and growing each time.
3. Add a few more — they should all appear when printed.
4. The input should clear after each click.

**Debugging Hints:**

* If nothing prints, check that both `addTask` and `printTasks` are correctly named and exist.
* If you see an error like “function not defined,” verify that Day 1 code is loaded *before* this script.
* If the input value logs correctly but the array doesn’t update, check that the global variable name matches exactly between files.

**If stuck, search / ask AI:**

* Search: “javascript call function on button click with input value”
* Ask AI: “How can I use a button click to call a function and pass an input value to it in JavaScript?”
