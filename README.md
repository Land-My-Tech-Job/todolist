## Activity Overview  

In this exercise you'll practice using variables, arrays, functions and objects to build a to-do list app

## Trello Board Link 
When finished please paste a link to your trello board here: 

## Activity Instructions

You will be building a to-do list app that includes: 

- An `h1` title
- A single `ul` tag, empty when the page is first loaded.
- A `form` for the user to add a new to-do, with a single text `input` and a `submit` button.

Make sure that your project includes all of the functionalities below:

- When the user writes something in the `form`'s text input area and clicks `submit`, the `ul` should update with a new `li` item at the bottom of the list. Keep in mind that the page should not refresh.

  <details>
    <summary>
      Hints/Steps
    </summary>
  
    1. Add an event listener to the form with `.addEventListener`. What event do you want to listen for?
    2. Grab the value the user typed from the text input.
    3. Create new `li` element with `document.createElement()`. Set its `textContent` property to be the text typed by the user
    4. Don't forget to append the created `li` to the list.

  </details>

- When the user writes _nothing_ in the `form`'s text input area and clicks `submit`, an error message (inside a `p` tag) should appear below the form.

  <details>
    <summary>
      Hints/Steps
    </summary>
  
    1. How can you check if the input text has something typed or not?
    2. Have an empty paragraph that is above the `<ul>` and under the `<form>`. If the user didn't type anything, modify the content of the paragraph to display a error message.

  </details>

- When the user clicks on one of the `li` items, the item should be crossed out, indicating that that to-do is complete. You will need to look at [`[element].style.textDecoration`](https://www.w3schools.com/jsref/prop_style_textdecoration.asp) for the cross out effect. Look at all the different text decoration options.

  <details>
    <summary>
      Hints/Steps
    </summary>
  
    1. You will need to add an event listener to all the `li` elements. What event do we want to listen for? What is a downside of this? Talk to a peer or ask an instructor.
    2. There is a better option than 1. Add the event listener to the list itself (parent of all `li`s) and take advantage of event bubbling. If you don't remember what this is check the [lecture video](https://www.youtube.com/watch?v=oAv9ND4fkAc&list=PLvQtbvxnE8UE8i2aog2lXWpREE5Br0yMB&index=6&t=2s) again.
    3. Once you know what element the event occurred on (`event.target`) check out [`[element].style.textDecoration`](https://www.w3schools.com/jsref/prop_style_textdecoration.asp) to put a line through the text and get the todo cross out effect.

  </details>

- Have the input go back to empty after adding a new todo.
- Implement a delete `button` next to each `li` that removes that `li` tag entirely.
- Clicking a todo that is crossed out (completed) uncrosses the todo.  
- Add the ability to add multiple to-dos if the user submits a text input with multiple lines. Each line should be a new to-do.
- Add some CSS styling to your app.
