# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨
<!DOCTYPE html>
<html>
  <head>
    <title>Hello World!</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
      <h1 class="title">Hello World! </h1>
      <p id="currentTime"></p>
      <script src="script.js"></script>
  </body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dynamic JavaScript Interaction</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1 id="heading">Welcome to My Webpage!</h1>
    <p id="paragraph">This paragraph will change.</p>
    <button id="changeTextButton">Change Text</button>
    <button id="toggleStyleButton">Change Style</button>
    <button id="addRemoveElementButton">Add/Remove Element</button>

    <div id="container"></div>

    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
}

h1 {
    color: blue;
}

button {
    margin: 10px;
    padding: 10px;
    background-color: #4CAF50;
    color: white;
    border: none;
    cursor: pointer;
}

button:hover {
    background-color: #45a049;
}
// Change text content dynamically when the button is clicked
document.getElementById('changeTextButton').addEventListener('click', function() {
    const paragraph = document.getElementById('paragraph');
    paragraph.textContent = 'The text has been changed dynamically!';
});

// Modify CSS styles via JavaScript when the button is clicked
document.getElementById('toggleStyleButton').addEventListener('click', function() {
    const heading = document.getElementById('heading');
    heading.style.color = heading.style.color === 'red' ? 'blue' : 'red';  // Toggle between red and blue
    heading.style.fontSize = heading.style.fontSize === '30px' ? '40px' : '30px';  // Toggle font size
});

// Add or remove an element when the button is clicked
document.getElementById('addRemoveElementButton').addEventListener('click', function() {
    const container = document.getElementById('container');
    
    // Check if the element already exists
    const newElement = document.getElementById('dynamicElement');
    if (newElement) {
        container.removeChild(newElement);  // Remove the element if it exists
    } else {
        const newElement = document.createElement('p');
        newElement.id = 'dynamicElement';
        newElement.textContent = 'This is a dynamically added paragraph!';
        container.appendChild(newElement);  // Add the new element to the container
    }
});



