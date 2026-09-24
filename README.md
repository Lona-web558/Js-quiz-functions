# Js-quiz-functions

# 🏆 Fill-in Quiz: 3 JavaScript Functions

A fill-in-the-blank quiz that tests your understanding of a simple web page with three JavaScript functions: **Add**, **Subtract** and **Multiply**.

Built with **HTML5, CSS3, Bootstrap 5 and vanilla JavaScript**, in a single file.

## Features

- 7 fill-in-the-blank questions about HTML, CSS and JavaScript
- Hint and explanation for every question
- Instant feedback (green for correct, red for incorrect)
- Progress bar and live score
- Final results screen with a review of missed answers
- "Try again" button
- Responsive layout, works on phones
- Light and dark mode support

## Files

```
fill-in-quiz.html   # the whole app (HTML + CSS + JS)
README.md           # this file
```

## Run locally

1. Download `fill-in-quiz.html`.
2. Double-click it to open in your browser. No build step or server needed.

## Deploy

The app is one static file, so it works on any static host.

- **Netlify:** drag and drop the file (rename it to `index.html` first).
- **Neocities:** upload the file as `index.html`.
- **Render:** create a new *Static Site* from your GitHub repo, with no build command and the publish directory set to `.`.

## Bootstrap

The file links Bootstrap 5.3 from the cdnjs CDN:

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.3/css/bootstrap.min.css">
```

A small Bootstrap-style fallback is also included in the `<style>` block, so the quiz still looks right if the CDN is blocked.

## Add or edit questions

Open the file and find the `QUESTIONS` array in the `<script>` section. Each question looks like this:

```js
{
  p: "Which window method displays the result to the user?",   // question text
  code: 'window.___("The sum is : " + num3);',                  // ___ marks each blank
  answers: [["alert"]],                                          // accepted answers per blank
  hint: "A pop-up with just an OK button.",
  why: "window.alert() shows a message box."                     // shown after checking
}
```

- Use `___` (three underscores) for every blank.
- `answers` has one list per blank, so a question with two blanks needs two lists, and any answer in a list is accepted.
- Answers are trimmed and not case-sensitive.

## Source page

The quiz is based on this page, which has three buttons that each call a function using `window.prompt()` and `window.alert()`:

```js
function add()      { /* num1 + num2 */ }
function minus()    { /* num1 - num2 */ }
function multiply() { /* num1 * num2 */ }
```

## License

Free to use and modify for learning and personal projects.
