1. Difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll:
* getElementById("id") → selects one element by its unique id.
* getElementsByClassName("class") → selects all elements with the given class. It returns an HTMLCollection(like an array but not exactly).
* querySelector("selector") → selects the first element that matches a CSS selector.
* querySelectorAll("selector") → selects all elements that match a CSS selector. It returns a NodeList (similar to an array).

2. How to create and insert a new element into the DOM:

// 1. Create a new element
const newDiv = document.createElement("div");

// 2. Add content or attributes
newDiv.textContent = "Hello, I am new!";
newDiv.className = "myClass";

// 3. Insert it into the DOM
document.body.appendChild(newDiv); // adds at the end of body

3. Event Bubbling and how it works:
* Event Bubbling is when an event starts at the target element and bubbles up to its parent elements.
* Example: If you click a button inside a div, the click happens on the button first, then the div, then the body.

4. Event Delegation in JavaScript and why it is useful:
* Event Delegation is when you attach an event listener to a parent instead of each child.
* Useful because:
    1. Works for dynamic elements added later.
    2. Saves memory by reducing multiple event listeners.
Example:

document.getElementById("parent").addEventListener("click", function(e) {
  if(e.target && e.target.tagName === "BUTTON") {
    console.log("Button clicked:", e.target.textContent);
  }
});

5. Difference between preventDefault() and stopPropagation() methods:
* preventDefault() → stops the default action of an element. Example: prevent a link from opening a page.
* stopPropagation() → stops the event from bubbling (or capturing) to parent elements.
