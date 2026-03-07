1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

ans : getElementById → it gets one element that has that specific id. Only one because ids are unique. Example: document.getElementById('myBtn') gives that button.
getElementsByClassName → gets all elements that have that class. But it gives us something like a list, not exactly an array. Example: document.getElementsByClassName('card') → all cards.
querySelector → kind of like a more flexible one. We can use any CSS selector and it gives only the first match. Example: document.querySelector('.card') → first card only.
querySelectorAll → same as querySelector but gives all matches. Example: document.querySelectorAll('.card') → all cards.


2. How do you create and insert a new element into the DOM?

ans : 1. Create the element first using document.createElement().

2. Add stuff to it if you want, like text or classes.


3. Pick where you want it to go in the page (the parent element) 

4. Insert it using appendChild or insertBefore.

3. What is Event Bubbling? And how does it work?

ans : Event bubbling is basically when you click on something inside another thing, the event “bubbles up” from the inside element to the outer elements.

example:
<div id="outer">
  <button id="btn">Click me</button>
</div>

If you click the button, first the button’s click happens.
Then the div’s click happens automatically, because the event bubbles up.

So it goes from the innermost element to the outer ones, like a bubble going up.

4. What is Event Delegation in JavaScript? Why is it useful?

ans : Event delegation is when instead of putting a click (or any event) on every single element, you put it on a parent, and then let the event bubble figure out which child was clicked.

We don’t need to attach a million event listeners which gives better performance
Works for elements added later dynamically too, because the parent is listening

5. What is the difference between preventDefault() and stopPropagation() methods?

ans : preventDefault() → stops the browser’s default action.
Like, if you click on a link <a> it normally goes to that URL
stopPropagation() → stops the event from bubbling up (or capturing down).
Like, if you click a button inside a div and the div has a click listener, normally both run.
