# 🌡️ Temperature Converter

A simple web app that converts temperatures between **Celsius**, **Fahrenheit** and **Kelvin**. Type a value into any one of the three boxes and the other two update automatically.

Built with plain HTML, CSS and JavaScript: no frameworks or libraries.

## Features

- Convert from any of the three scales into the other two
- Results rounded to two decimal places
- Responsive, centred card layout with a gradient background
- No dependencies, so it runs straight in the browser

## How it works

Each input field has an `onchange` listener that calls `computeTemp(event)`. The function reads the value that was entered, checks which field it came from using `event.target.name`, and uses a `switch` statement to apply the right formulas:

| From       | To Celsius        | To Fahrenheit      | To Kelvin    |
|------------|-------------------|--------------------|--------------|
| Celsius    | —                 | `C × 1.8 + 32`     | `C + 273.15` |
| Fahrenheit | `(F − 32) ÷ 1.8`  | —                  | `(F − 32) ÷ 1.8 + 273.15` |
| Kelvin     | `K − 273.15`      | `(K − 273.15) × 1.8 + 32` | — |

## Project structure

```
temperature-converter/
├── index.html   # Page structure and the three input fields
├── style.css    # Layout, gradient background and input styling
└── app.js       # Conversion logic
```

## Built with

- HTML5
- CSS3
- JavaScript (ES6)

## Possible improvements

- Update results live as you type (using the `input` event instead of `change`)
- Add a "clear" button to reset all fields
- Warn when a value goes below absolute zero
