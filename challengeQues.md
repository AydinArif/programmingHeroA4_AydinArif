# Questions

1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?
2. How do you create and insert a new element into the DOM?
3. What is Event Bubbling? And how does it work?
4. What is Event Delegation in JavaScript? Why is it useful?
5. What is the difference between preventDefault() and stopPropagation() methods?

# Answers

1. So basically we think of getElementById as searching for a specific person by their Social Security number—it only finds one specific thing. getElementsByClassName is like looking for everyone wearing a blue shirt. Most people just use querySelector or querySelectorAll though, because that lets you use CSS-style names (like .class or #id), which is way more flexible.


2. This is a two-step process. First, we "spawn" the element in the code using document.createElement('div'). At this point, it exists in memory but not on the page. To actually see it, we have to use appendChild() or prepend() to stick it inside a parent element, like the "body" or a specific "div".

3. Event bubbling is like when you click a button that’s inside a div, the click "bubbles up." The button feels the click first, then the div feels it, then the body feels it. It’s like a ripple moving outward from where you dropped a stone in a pond.

4. Event delegation is like imagine instead of putting a click listener on 100 different list items (which slows down a site), you just put one listener on the parent container. Its useful since the clicks bubble up anyway, the parent can catch them and figure out which specific item was actually clicked.

5. preventDefault() tells the browser, "Don't do your normal job" (like stopping a link from opening or a form from refreshing). stopPropagation() tells the event, "Stop right here!" It prevents the event from bubbling up to any parent elements.
