# Guitar Tutor Landing Page

![image](https://github.com/01cheese/Lending-for-guitar/assets/115219323/9cc202d0-a78a-497a-8bdc-bde2dd7d2724)

Welcome to the Guitar Tutor Landing Page project. This README will provide an extensive overview of the project, including setup instructions, an overview of the file structure, code examples, explanations, and additional resources.

## Table of Contents

1. [Project Overview](#project-overview)
2. [File Structure](#file-structure)
3. [Setup Instructions](#setup-instructions)
4. [Code Explanation](#code-explanation)
   - [HTML](#html)
   - [CSS](#css)
   - [JavaScript](#javascript)
5. [Responsive Design](#responsive-design)
6. [Best Practices](#best-practices)
7. [Examples](#examples)
8. [Resources](#resources)
9. [Conclusion](#conclusion)

## Project Overview

This project is a landing page for a guitar tutor named James. The page includes sections about James's teaching experience, the types of guitars he teaches, and an option to book lessons. The landing page is designed to be responsive and visually appealing, incorporating modern web development practices.

## File Structure

- **index.html**: The main HTML file containing the structure of the webpage.
- **style.css**: The main CSS file managing the appearance of the page.
- **reset1.css**: CSS reset file to remove default browser styling.
- **normalize1.css**: CSS file to make browsers render all elements more consistently and in line with modern standards.
- **script.js**: JavaScript file adding interactivity to the page.
- **style.css.map**: Source map file for `style.css`.
- **reset1.css.map**: Source map file for `reset1.css`.
- **normalize1.css.map**: Source map file for `normalize1.css`.

## Setup Instructions

1. Clone the repository to your local machine:
   ```bash
   git clone <repository_url>
   ```
2. Navigate to the project directory:
   ```bash
   cd guitar-tutor-landing-page
   ```
3. Open the `index.html` file in your preferred web browser.

## Code Explanation

### HTML

The `index.html` file provides the structure of the webpage. Key components include:

- **Header and Navigation**:
  ```html
  <header class="main-section__header">
    <a href=""><img src="icons/logo.svg" alt="Лого" class="main-section__logo" /></a>
    <nav class="main-section__nav nav-menu">
      <ul class="nav-menu__list">
        <li class="nav-menu__list-item"><a href="#about-me">About me</a></li>
        <li class="nav-menu__list-item"><a href="#classes">Classes</a></li>
        <li class="nav-menu__list-item"><a href="#appointment">Appointment</a></li>
      </ul>
    </nav>
  </header>
  ```
  This section contains the logo and the navigation menu.

- **Main Content**:
  ```html
  <div class="container main-section__content-container">
    <div class="left-wrapper">
      <img src="img/guitarist.png" alt="Фото гитариста" class="left-wrapper__img" />
      <!-- More content here -->
    </div>
    <div class="right-wrapper">
      <h1 class="right-wrapper__title title">I am James</h1>
      <p class="right-wrapper__text">Guitar tutor with seven years of teaching experience</p>
      <div class="right-wrapper__button buttons">
        <button class="buttons__main-btn">Book<br />lesson</button>
        <div class="right-wrapper__icon-btn buttons__icon-btn">
          <img src="icons/Иконка чата 1.svg" alt="Чат" />
          <p class="buttons__text">Have questions?</p>
        </div>
      </div>
    </div>
  </div>
  ```
  This section includes the main promotional content with images and text.

- **Footer**:
  ```html
  <footer id="appointment" class="footer-section">
    <div class="footer-section__content-container container">
      <div class="footer-section__left-wrapper">
        <img src="img/Гриф 1.png" alt="" class="footer-section__img" />
      </div>
      <div class="footer-section__right-wrapper">
        <h2 class="footer-section__title title">Sign up for a<br />trial lesson</h2>
        <div class="footer-section__icons-box icons">
          <div class="icons__item"><i class="fa-brands fa-skype"></i></div>
          <div class="icons__item"><i class="fa-brands fa-twitter"></i></div>
          <div class="icons__item"><i class="fa-brands fa-telegram"></i></div>
          <div class="icons__item"><i class="fa-brands fa-instagram"></i></div>
        </div>
      </div>
    </div>
  </footer>
  ```
  This section includes a call to action for signing up for a trial lesson and social media links.

### CSS

The `style.css` file contains styles that define the look and feel of the webpage. Key sections include:

- **Base Styles**:
  ```css
  html {
    line-height: 1.15;
    -webkit-text-size-adjust: 100%;
  }

  body {
    margin: 0;
  }

  main {
    display: block;
  }
  ```

- **Layout and Positioning**:
  ```css
  .container {
    position: relative;
    max-width: 1140px;
    margin: 0 auto;
  }

  .main-section {
    position: relative;
    min-height: 800px;
    padding-top: 16px;
    background-color: #F0F0F0;
    overflow: hidden;
    margin-bottom: 32px;
  }
  ```

- **Buttons and Interactivity**:
  ```css
  .buttons {
    display: flex;
  }
  
  .buttons__main-btn {
    margin-right: 32px;
    width: 200px;
    height: 60px;
    background-color: #F28B64;
    color: white;
    border-radius: 100px;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    font-size: 18px;
  }
  ```

### JavaScript

The `script.js` file adds interactivity to the webpage. For example, it handles the hamburger menu toggle:

```javascript
window.addEventListener('DOMContentLoaded', () => {
  const menu = document.querySelector('.nav-menu'),
        menuItem = document.querySelectorAll('.nav-menu__list-item'),
        hamburger = document.querySelector('.hamburger');

  hamburger.addEventListener('click', () => {
    hamburger.classList.toggle('hamburger_active');
    menu.classList.toggle('nav-menu_active');
  });

  menuItem.forEach(item => {
    item.addEventListener('click', () => {
      hamburger.classList.toggle('hamburger_active');
      menu.classList.toggle('nav-menu_active');
    });
  });
});
```

This code listens for a click event on the hamburger icon to toggle the active class, which opens and closes the mobile navigation menu.

## Responsive Design

The CSS includes media queries to ensure the landing page is responsive and looks good on all device sizes:

```css
@media (max-width: 1199px) {
  .container {
    width: 960px;
  }
  .left-wrapper img {
    width: 750px;
    height: auto;
  }
  .left-wrapper__rectangle-blue {
    width: 500px;
    height: 200px;
  }
  .left-wrapper__rectangle-orange {
    width: 550px;
    height: 200px;
  }
  .left-wrapper__rectangle-grey {
    width: 500px;
    height: 200px;
  }
  .right-wrapper {
    right: 20px;
  }
  .main-section {
    min-height: 690px;
  }
  .main-section__first-elipse {
    right: 10px;
  }
  .main-section__second-elipse {
    top: 560px;
  }
  .guitar-box {
    width: 300px;
    height: 300px;
  }
  .guitar-box__text {
    top: 110px;
    left: 120px;
  }
  .achievement-box__number {
    font-size: 36px;
  }
  .achievement-box__text {
    font-size: 16px;
  }
  .third-section__left-wrapper {
    padding-left: 40px;
  }
  .third-section__left-title {
    margin-right: 20px;
  }
  .footer-section__img {
    width: 600px;
    height: auto;
  }
}
```

These media queries adjust the layout and size of elements for different screen sizes to ensure the content is readable and visually appealing on devices ranging from desktops to smartphones.

## Best Practices

- **Semantic HTML**: Use semantic HTML tags such as `<header>`, `<nav>`, `<section>`, and `<footer>` to improve the accessibility and SEO of your webpage.
- **Responsive Design**: Implement responsive design using CSS media queries to ensure your website looks good on all devices.
- **JavaScript for Interactivity**: Use JavaScript to add interactive elements

 to your website, enhancing user engagement.
- **CSS Reset and Normalize**: Use CSS reset and normalize files to ensure consistent styling across different browsers.

## Examples

To see the landing page in action, open the `index.html` file in your web browser. Here are a few highlights:

- **Responsive Navigation**: The navigation menu collapses into a hamburger menu on smaller screens.
- **Dynamic Content**: The page includes dynamic elements such as images and text that adapt to different screen sizes.
- **Interactive Elements**: The JavaScript code enables interactivity, such as the hamburger menu toggle.

## Resources

- [MDN Web Docs](https://developer.mozilla.org/en-US/)
- [W3Schools](https://www.w3schools.com/)
- [CSS-Tricks](https://css-tricks.com/)
- [JavaScript.info](https://javascript.info/)
- [Font Awesome](https://fontawesome.com/)

## Conclusion

This project demonstrates a modern, responsive landing page for a guitar tutor. It uses HTML, CSS, and JavaScript to create an engaging user experience.
