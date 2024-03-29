## The Golden Rule: 

🦸 🦸‍♂️ `Stop starting and start finishing.` 🏁

If you work on more than one feature at a time, you are guaranteed to multiply your bugs and your anxiety.

## Making a plan

1) **Make a drawing of your app. Simple "wireframes"**
   Drawing of wireframe in notebook

2) **Once you have a drawing, name the HTML elements you'll need to realize your vision**
  1. Div for defeated goblins
     - Why: to display the defated goblins
     - How: html div
  2. Div for fighter
      - Why: to display "You" and your information 
      - How: html div
     1. image
         - why: to give the user character an image
     2. div for Hp
         - why: to display hp
     4. div for game over message
         - why: to display game over message
  3. Form for challenge goblin
     - why: to create more goblins
     - how: form
     1. input for goblin name
          - why: to let the user name a goblin
          - How: input field
     3. button to submit goblin
          - why: so the user can submit their goblin names
          - How: submit button
  4. Div for goblins
     - why: so the goblins (with their names and hp) the user is fighting can be    displayed
     - how: html
  
3) **For each HTML element ask: Why do I need this? (i.e., "we need div to display the results in")** 
4) **Once we know _why_ we need each element, think about how to implement the "Why" as a "How" (i.e., `resultsEl.textContent = newResults`)**
5) **Find all the 'events' (user clicks, form submit, on load etc) in your app. Ask one by one, "What happens when" for each of these events. Does any state change?**
      1. Each goblin is clickable
          - possibly decrmement this goblin's HP
          - possibly decrment player HP
          - possibly increment defeatedGoblins
          - update the DOM with new goblin, player, and defeated goblin state. (render deated goblins differently)

      2. New goblin form
          - User has supplied a name and submitted the form
          - Make a new goblin object with that user input
          - Add that object to the array of goblins in state
          - "update a list"
          - clear out the list DOM
          - loop through the goblins
          - render a new goblin DOM element for each item
          - append that element to the HTML

1) **Think about how to validate each of your features according to a Definition of Done. (Hint: console.log usually helps here.)**

2) **Consider what features _depend_ on what other features. Use this dependency logic to figure out what order to complete tasks.**

Additional considerations:
- Ask: which of your HTML elements need to be hard coded, and which need to be dynamically generated?
- Consider your data model. 
  - What kinds of objects (i.e., Dogs, Friends, Todos, etc) will you need? 
  - What are the key/value pairs? 
  - What arrays might you need? 
  - What needs to live in a persistence layer?
- Is there some state we need to initialize?
- Ask: should any of this work be abstracted into functions? (i.e., is the work complicated? can it be resused?)
