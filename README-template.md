# Frontend Mentor - Results summary component solution

This is a solution to the [Results summary component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/results-summary-component-CE_K6s0maV). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

### Screenshot




### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [https://results-component-practice.netlify.app/](https://results-component-practice.netlify.app/)

## My process

### Built with

- HTML, CSS, JS
- Flexbox
- CSS Grid

### What I learned

Through this project, I learned how to take data from a .json file and added to the html in a new div with a prebuilt class using a little bit of JS.

```js
const listEl = document.querySelector("div.summary__cards");
      fetch('./data.json')
          .then(res => res.json())
          .then(data => {
            data.forEach(element => {
              listEl.insertAdjacentHTML('beforeend', `<div class="summary__category">
                                                        <div class="category__title">
                                                          <img class="category__title--icon" src="${element.icon}" alt="icon">
                                                          <p class="category__title--name">${element.category}</p>
                                                        </div>
                                                        <p class="summary__category--score">${element.score}<span> / 100</span></p>
                                                      </div>`);
            });
          });
```

### Useful resources

- [Video "Read JSON File into HTML with JavaScript Fetch API"](https://www.youtube.com/watch?v=Oage6H4GX2o) - This helped me to understand how to read the data from a JSON file and added to the HTML with javascript.

## Author

- Linkedin - [Juan José Potes Gómez](https://www.linkedin.com/in/juan-jose-potes-gomez/)
- Frontend Mentor - [@J-Potes](https://www.frontendmentor.io/profile/J-Potes)
- Github - [@J-Potes](https://github.com/J-Potes)
