🛠 Broken Pricing Card Refactor – AI Assisted
📌 Project Overview

This project focuses on fixing, refactoring, and improving a broken pricing card web component using AI assistance (Cursor AI).

The original component had:

Layout issues

CSS typos

Invalid HTML structure

Poor reusability

Unresponsive button behavior

The goal was to:

Identify and fix the bugs

Improve styling and layout

Refactor into a reusable component

Prepare clean, production-ready code

🚨 Issues Found in the Original Code
1️⃣ CSS Errors

box-shdow → typo (should be box-shadow)

No border radius

No cursor pointer on button

No transition effects

2️⃣ HTML Errors

<h2> tag was not properly closed

Missing responsive meta tag

No semantic improvements

3️⃣ UX Issues

Button not clearly interactive

Layout not centered properly on all screens

No hover animation smoothness

🤖 AI Prompt Used in Cursor
Fix layout bugs in this pricing card component. 
Correct HTML and CSS errors. 
Improve styling and responsiveness. 
Refactor it into a reusable component structure like Card(title, price, features). 
Make it clean and production-ready.

❌ BEFORE (Broken Code)

Issues included:

Typo in box-shadow

Unclosed <h2> tag

No responsiveness improvements

Not reusable

(Original snippet provided in the instructions)

✅ AFTER (Refactored & Reusable Version)
✨ Improvements Made

Fixed CSS typo

Fixed broken HTML structure

Added responsive meta tag

Improved spacing and alignment

Added hover transitions

Added cursor pointer

Centered layout using Flexbox

Converted into reusable Card() function

Clean and reusable structure

💻 Refactored Code
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Reusable Pricing Card</title>

<style>
body {
  font-family: Arial, sans-serif;
  background: #f4f4f4;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.pricing {
  width: 300px;
  background-color: #fff;
  box-shadow: 0 0 10px #ccc;
  padding: 20px;
  border-radius: 8px;
  text-align: center;
}

.title {
  font-size: 22px;
  font-weight: bold;
  margin-bottom: 10px;
}

.price {
  font-size: 20px;
  color: green;
  margin-bottom: 15px;
}

.features {
  list-style: none;
  padding-left: 0;
  margin-bottom: 15px;
}

.features li {
  padding: 6px;
  border-bottom: 1px solid #eee;
}

.btn {
  background: blue;
  color: white;
  padding: 10px 20px;
  border: none;
  margin-top: 10px;
  cursor: pointer;
  border-radius: 4px;
  transition: background 0.3s ease;
}

.btn:hover {
  background: darkblue;
}
</style>
</head>

<body>

<div id="card-container"></div>

<script>
function Card(title, price, features) {
  const featureItems = features
    .map(feature => `<li>${feature}</li>`)
    .join("");

  return `
    <div class="pricing">
      <h2 class="title">${title}</h2>
      <p class="price">${price}</p>
      <ul class="features">
        ${featureItems}
      </ul>
      <button class="btn">Start Trial</button>
    </div>
  `;
}

document.getElementById("card-container").innerHTML =
  Card("Basic Plan", "$9.99 / month", [
    "1 GB Storage",
    "Basic Support",
    "All Core Features"
  ]);
</script>

</body>
</html>

🧩 Refactoring Strategy

Separated structure from data

Used a function to generate reusable components

Improved maintainability

Made it scalable for multiple pricing plans

Example reuse:

Card("Pro Plan", "$19.99 / month", [...])
Card("Enterprise Plan", "$49.99 / month", [...])

📚 Skills Practiced

Debugging HTML & CSS

Refactoring legacy code

Component-based thinking

AI-assisted development workflow

Improving UI/UX

Writing reusable JavaScript functions

🚀 Final Outcome

The broken pricing card was successfully:

Fixed

Improved

Refactored

Made reusable

Styled professionally

Tested and functional
