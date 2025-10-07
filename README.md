# Simple-Calculator

Dear Developer,

I'm here to help you understand how your simple calculator project is put together. It's built using three main ingredients: HTML, CSS, and JavaScript. Think of it like building a small, interactive gadget!

### 1. HTML (`index.html`) - The Skeleton

First, we have your [`index.html`](index.html:1) file. This is the **structure** of your calculator. Imagine it as the bones and frame of a house.

-   It sets up the basic webpage.
-   You'll see an `<input type="text" id="inputBox" placeholder="0">`. This is the **calculator screen** where numbers appear. The `id="inputBox"` is like a unique name tag, so our JavaScript can easily find and update this screen.
-   Below that, you have all your **buttons** (`<button>`). These are for numbers (0-9), math operations (+, -, *, /, %), "AC" (All Clear), "DEL" (Delete), and the all-important "=" (Equals) button.
-   Crucially, at the very bottom of the `<body>`, you'll find `<script src="script.js"></script>`. This line **connects your JavaScript file** to your HTML, bringing your calculator to life!

### 2. CSS (`style.css`) - The Style

Next up is your [`style.css`](style.css:1) file. This is all about making your calculator **look good** – it's the paint, wallpaper, and furniture for our house!

-   It sets the **background** of your entire webpage to a cool gradient.
-   It styles the main **calculator box** itself, giving it a nice border, rounded corners, and a subtle shadow to make it pop.
-   The **display screen** (`input`) is styled to be large, white, and to show text aligned to the right, just like a real calculator.
-   All the **buttons** are made round, with white text, and a soft shadow.
-   Special buttons like the **equals button** (`.equalBtn`) get a distinct orange color, and the **operator buttons** (`.operator`) turn green, making them easy to spot.

### 3. JavaScript (`script.js`) - The Brains

Finally, we have your [`script.js`](script.js:1) file. This is the **brain** of your calculator, making everything interactive and functional. This is where the magic happens when you press buttons!

-   **Finding the Screen:** `let input = document.getElementById('inputBox');` This line tells JavaScript, "Go find the element with the ID 'inputBox' (our screen) and let me control it."
-   **Finding the Buttons:** `let buttons = document.querySelectorAll('button');` This gathers all the buttons on your calculator so JavaScript can listen to them.
-   **Remembering Your Input:** `let string = "";` This variable is like a notepad where JavaScript keeps track of all the numbers and operations you've typed so far (e.g., "1+2*3").
-   **Listening for Clicks:** The code then goes through *each* button and says, "Hey, if someone clicks you, do something!"
    -   **If you click `=`:** JavaScript takes everything on its notepad (`string`), figures out the math (using `eval()`), and then writes the final answer onto the calculator screen (`input.value = string;`).
    -   **If you click `AC` (All Clear):** It simply erases everything from the notepad (`string = "";`) and clears the screen.
    -   **If you click `DEL` (Delete):** It removes the very last character you typed from the notepad and updates the screen.
    -   **If you click any other number or operator:** It adds that number or symbol to the notepad (`string += e.target.innerHTML;`) and shows it on the screen, so you can see what you're typing.

So, in a nutshell:
-   **HTML** gives your calculator its shape.
-   **CSS** makes it look stylish.
-   **JavaScript** makes it actually calculate and respond to your touches!

I hope this explanation helps you understand your calculator project better!

Best regards,

Kilo Code
