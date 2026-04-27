# p_d__html_css

📄 Documentation – Landing Page “Rock Band”

 1. General Description

This project is a rock band landing page, built using:

HTML → structure

CSS → styling and layout

JavaScript → scroll animation


The page includes:

A visual background

Navigation menu

Rock introduction

Events table

History section

Image gallery



---

 2. HTML Structure

🔹 <!DOCTYPE html>

Defines the document as HTML5.


---

🔹 <head>

Contains configuration:

meta charset="UTF-8" → supports special characters

meta viewport → makes the page responsive

<title> → browser tab title

<link> → connects the CSS file



---

🔹 <body>

Contains all visible content.


---

 Background section

<section class="fondo"></section>

Used as the main background

Controlled by JavaScript (zoom + fade effect)



---

Header

<header>
  <h1>ROCK BAND</h1>
  <nav>...</nav>
</header>

Contains the main title and navigation menu



---

 Menu

<ul class="menu">

Links to sections using #id


 Issue:

href="#start" does not match id="Start" (case-sensitive)



---

 Start Section

<section id="Start">

Introductory text



---

 Events Section

<section id="envents">

 Typo: should be events

Contains a table with bands:

The Beatles

Queen

Led Zeppelin

Pink Floyd

Metallica



---

 History Section

<section id="history">

Explains rock evolution

Includes text and image


 Issue:

<div class="contendor">

→ should be contenedor


---

Gallery

<section class="galeria">

Displays images in a row



---

 Footer

<footer>

Final text of the page



---

 3. CSS Styles

🔹 Reset

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

Removes default spacing

Improves layout control



---

🔹 Body

body {
  background: #290909e3;
  color: white;
}

Dark rock-style theme



---

🔹 Background

section.fondo {
  background-image: url(...);
  height: 100vh;
}


---

🔹 Menu (Flexbox)

.menu {
  display: flex;
  justify-content: center;
}

Horizontal layout



---

🔹 Sections

section {
  padding: 40px;
  text-align: center;
}


---

🔹 Table

table {
  width: 100%;
}


---

🔹 Gallery

.imagenes {
  display: flex;
}


---

🔹 Responsive Design

@media (max-width: 768px)

Applies when screen is small:

Changes:

Menu → vertical

Images → column

Layout → adaptive



---

⚙️ 4. JavaScript (Animation)

🔹 Variables

let fondo = document.querySelector('.fondo');


---

🔹 Function

function updatefondo()

What it does:

Detects scroll position

Calculates:

Scale (zoom)

Opacity (fade)




---

🔹 Effect

fondo.style.transform = `scale(...)`
fondo.style.opacity = ...

 Result:

On scroll:

Background zooms in

Background fades out




---

🔹 Optimization

requestAnimationFrame()

Makes animation smoother

Improves performance




 Conclusion

Your project: ✔ Uses semantic HTML
✔ Implements Flexbox
✔ Has responsive design
✔ Includes JavaScript animation

