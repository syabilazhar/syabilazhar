```html
/ra<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>HATI</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div class="wrapper">
      <h2 class="question">I suka you</h2>
      <img
        class="gif"
        alt="gif"
        src="https:/w.githubusercontent.com/DzarelDeveloper/Img/main/gifyou.webp"
      />
      <div class="btn-group">
        <button class="yes-btn">accept</button>
        <button class="no-btn">sorry reject</button>
      </div>
    </div>
    <script src="script.js"></script>
  </body>
</html>

```

```css
/* Resetting default margin, padding, and box-sizing */
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Styling the body */
body {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background: whitesmoke;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
}

/* Styling the gif */
.gif {
  height: 100%;
  width: 100%;
}

/* Styling the h2 element */
h2 {
  text-align: center;
  font-size: 1.5em;
  color: #e94d58;
  margin: 15px 0;
}

/* Styling the button group */
.btn-group {
  width: 100%;
  height: 50px;
  display: flex;
  justify-content: center;
  margin-top: 50px;
}

/* Styling the buttons */
button {
  position: relative; /* Changed from absolute to relative */
  width: 150px;
  height: inherit;
  color: white;
  font-size: 1.2em;
  border-radius: 30px;
  outline: none;
  cursor: pointer;
  box-shadow: 0 2px 4px gray;
  border: 2px solid #e94d58;
}

/* Styling the first button in the group */
button:nth-child(1) {
  margin-right: 10px; /* Adjusted margin */
  background: #e94d58;
}

/* Styling the second button in the group */
button:nth-child(2) {
  margin-left: 10px; /* Adjusted margin */
  background: white;
  color: #e94d58;
}

```

```js
const wrapper = document.querySelector(".wrapper");
const question = document.querySelector(".question");
const gif = document.querySelector(".gif");
const yesBtn = document.querySelector(".yes-btn");
const noBtn = document.querySelector(".no-btn");

yesBtn.addEventListener("click", () => {
  question.innerHTML = "Aaaaa, umiii adik kena accept.. dah bubye";
  gif.src =
    "https://raw.githubusercontent.com/DzarelDeveloper/Img/main/gif.webp";
});

noBtn.addEventListener("mouseover", () => {
  const noBtnRect = noBtn.getBoundingClientRect();
  const maxX = window.innerWidth - noBtnRect.width;
  const maxY = window.innerHeight - noBtnRect.height;
  const randomX = Math.floor(Math.random() * maxX);
  const randomY = Math.floor(Math.random() * maxY);

  noBtn.style.left = randomX + "px";
  noBtn.style.top = randomY + "px";
});

```
