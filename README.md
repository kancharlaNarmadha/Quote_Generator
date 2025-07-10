
# Quote_Generator
## Date:10.07.2025
## Objective:
To create a simple quote generator using HTML, CSS, and JavaScript that displays a new random motivational quote each time a button is clicked — similar to daily quote sections on blogs or productivity apps.

## Tasks:

#### 1. Create the HTML Structure:
Add a heading like ```<h1>InspireMe</h1>```

Use a ```<div> or <p>``` to display the quote text.

Use another ```<p> or <span>``` to display the author’s name.

Add a button labeled “Get Quote”.

#### 2. Style the Layout Using CSS:
Center everything on the page using flexbox.

Style the quote box with padding, background color, and rounded borders.

Use a clean font (like Roboto or Open Sans).

Add hover effects for the button.

#### 3. Add JavaScript Functionality:
Store an array of quotes (objects with text and author).

On button click, generate a random index using Math.random().

Display the selected quote and author in the HTML.

Ensure each click updates the quote dynamically using innerText.

#### 4. Enhancements:
Animate the quote change using fade effects.

Add a “Tweet this” button with a share link.
## HTML Code:
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>InspireMe</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="quote-box">
    <h1>InspireMe 💡</h1>
    <p id="quote">Click the button to get inspired!</p>
    <span id="author">—</span>
    <button id="new-quote">Get Quote</button>
  </div>

  <script src="script.js"></script>
</body>
</html>

```
## CSS Code:
```
body {
  margin: 0;
  padding: 0;
  font-family: 'Open Sans', sans-serif;
  background-color: #f0f8ff;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.quote-box {
  text-align: center;
  background-color: #ffffff;
  padding: 30px;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  max-width: 400px;
  width: 90%;
}

h1 {
  color: #333;
  margin-bottom: 20px;
}

#quote {
  font-size: 18px;
  color: #555;
  margin: 20px 0 10px;
}

#author {
  display: block;
  font-weight: bold;
  color: #888;
  margin-bottom: 20px;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  border: none;
  background-color: #0077cc;
  color: white;
  border-radius: 6px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #005fa3;
}

```
## Javascript Code:
```
const quotes = [
  { text: "Believe you can and you're halfway there.", author: "Theodore Roosevelt" },
  { text: "Your limitation—it’s only your imagination.", author: "Unknown" },
  { text: "Push yourself, because no one else is going to do it for you.", author: "Unknown" },
  { text: "Great things never come from comfort zones.", author: "Unknown" },
  { text: "Dream it. Wish it. Do it.", author: "Unknown" },
];

const quoteText = document.getElementById("quote");
const authorText = document.getElementById("author");
const newQuoteBtn = document.getElementById("new-quote");

newQuoteBtn.addEventListener("click", () => {
  const randomIndex = Math.floor(Math.random() * quotes.length);
  const quote = quotes[randomIndex];

  quoteText.style.opacity = 0;
  authorText.style.opacity = 0;

  setTimeout(() => {
    quoteText.innerText = quote.text;
    authorText.innerText = `— ${quote.author}`;
    quoteText.style.opacity = 1;
    authorText.style.opacity = 1;
  }, 300);
});

```
## Output:-
<img width="812" height="580" alt="image" src="https://github.com/user-attachments/assets/0c2b5a66-eafc-47e3-9b16-7b87b9c20bf1" />


## Result:
A simple quote generator using HTML, CSS, and JavaScript that displays a new random motivational quote each time a button is clicked — similar to daily quote sections on blogs or productivity apps is created successfully.
