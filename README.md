# My First README
##### Repo explaining README.md



### Steps to install Tic Tac Toe to computer
1. Go to [Repo](https://github.com/anonyymous1/tic-tac-toe).
2. `Fork` page.
3. `Clone` code.
4. Open iTerm2 .
5. Type - `git clone https://github.com/anonyymous1/tic-tac-toe` into iTerm2.
6. Open `index.html` by typing `open index.html` in iTerm2.

# Table of Contents

1. [HTML](#HTML)
2. [CSS](#CSS)
3. [JavaScript](#Javascript)
4. [Functions](#Functions)

## HTML
```HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Tic Tac Toe</title>
  <link rel="stylesheet" type="text/css" href="css/style.css">
  <style>@import url('https://fonts.googleapis.com/css2?family=Rock+Salt&display=swap');</style>
  <style>@import url('https://fonts.googleapis.com/css2?family=Caveat+Brush&family=Rock+Salt&display=swap');</style>
</head>
<body>
  <h1>Tic-Tac-Toe</h1>
  
  <h3 id="player">Player 1's Turn (X)</h3>
  <div class="winTrack">
    <h2 id="pow">Player One Wins</h2>
    <h2 id="ptw">Player Two Wins</h2>
  </div>
  <div class="grid">
  <div id="sq1" class="cell"><p> </p></div>
  <div id="sq2" class="cell"><p>  </p></div>
  <div id="sq3" class="cell"><p>   </p></div>
  <div id="sq4" class="cell"><p>    </p></div>
  <div id="sq5" class="cell"><p>     </p></div>
  <div id="sq6" class="cell"><p>      </p></div>
  <div id="sq7" class="cell"><p>       </p></div>
  <div id="sq8" class="cell"><p>        </p></div>
  <div id="sq9" class="cell"><p>         </p></div>
  </div>
  <div class="textDiv">
    <h4 id="output">Choose a square!</h4>
    <h5 id="gameOver"></h5>
    <input type="button" value="Reset Game" id="clear">
  </div>

  <script type="text/javascript" src="js/app.js"></script>
</body>
</html>
```

## CSS
```CSS
h1 {
  color: whitesmoke;
  font-size: 60px;
  margin: 0px; 
  font-family: 'Caveat Brush', cursive;
  text-align: center;
}

h3 {
  color: whitesmoke;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  text-align: center;
}

h4 {
  color: green; 
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  text-align: center;
}

h5 { 
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  text-align: center;
  padding-bottom: 0%;
}

.winTrack {
  display: flex;
}

h2 {
  font-family: 'Rock Salt', cursive;
  font-size: 12px;
  color: whitesmoke;
}

#ptw {
  position: relative;
  margin-left: 90px;
}

#pow {
  position: relative;
  margin-left: 80px;
}


.grid {
  display: grid;
  grid-gap: 2px;
  grid-template-rows: 100px 100px 100px;
  grid-template-columns: 100px 100px 100px;
  justify-content: center;
  padding: 5px;
}

#sq1, #sq2, #sq3, #sq4, #sq5, #sq6, #sq7, #sq8, #sq9 {
  border: 1px solid white;
  border-radius: 25px;
  display: inline-block;
}

.cell {
  border-color: 1px dotted white;
  color: white;
  text-align: center;
  font-size: 40px;
  font-family: 'Rock Salt', cursive;
}

#clear {
  position: relative;
  left: 50%;
  transform: translateX(-50%);
}

body {
  background-image: url("https://i.pinimg.com/originals/34/6e/73/346e73fa85fbc021939576a834fd7e42.jpg");
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: 100% 100%;
}
```

## JS

```Javascript
console.log('Hello Front End');

/*------------------------------CONSTANTS------------------------------*/
const sq1 = document.querySelector('#sq1');
const sq2 = document.querySelector('#sq2');
const sq3 = document.querySelector('#sq3');
const sq4 = document.querySelector('#sq4');
const sq5 = document.querySelector('#sq5');
const sq6 = document.querySelector('#sq6');
const sq7 = document.querySelector('#sq7');
const sq8 = document.querySelector('#sq8');
const sq9 = document.querySelector('#sq9');
const cell = document.querySelector('.cell');
const playersTurn = document.querySelector('#player');
const output = document.querySelector('#output');
const clear = document.querySelector('#clear');
const gameOver = document.querySelector('#gameOver');
const pow = document.querySelector('#pow');



/*---------------------------EVENT LISTENERS---------------------------*/

document.querySelector('#sq1').addEventListener("click", function () {
      if (playersTurn.textContent === "Player 1's Turn (X)") {
        changeToX(sq1);
      } else if (playersTurn.textContent === "Player 2's Turn (O)") {
        changeToO(sq1);
}      
})

document.querySelector('#sq2').addEventListener("click", function () {
  if (playersTurn.textContent === "Player 1's Turn (X)") {
    changeToX(sq2);
  } else if (playersTurn.textContent === "Player 2's Turn (O)") {
    changeToO(sq2);
}      
})

document.querySelector('#sq3').addEventListener("click", function () {
  if (playersTurn.textContent === "Player 1's Turn (X)") {
    changeToX(sq3);
  } else if (playersTurn.textContent === "Player 2's Turn (O)") {
    changeToO(sq3);
}      
})

document.querySelector('#sq4').addEventListener("click", function () {
  if (playersTurn.textContent === "Player 1's Turn (X)") {
    changeToX(sq4);
  } else if (playersTurn.textContent === "Player 2's Turn (O)") {
    changeToO(sq4);
}      
})

document.querySelector('#sq5').addEventListener("click", function () {
  if (playersTurn.textContent === "Player 1's Turn (X)") {
    changeToX(sq5);
  } else if (playersTurn.textContent === "Player 2's Turn (O)") {
    changeToO(sq5);
}      
})

document.querySelector('#sq6').addEventListener("click", function () {
  if (playersTurn.textContent === "Player 1's Turn (X)") {
    changeToX(sq6);
  } else if (playersTurn.textContent === "Player 2's Turn (O)") {
    changeToO(sq6);
}      
})

document.querySelector('#sq7').addEventListener("click", function () {
  if (playersTurn.textContent === "Player 1's Turn (X)") {
    changeToX(sq7);
  } else if (playersTurn.textContent === "Player 2's Turn (O)") {
    changeToO(sq7);
}      
})

document.querySelector('#sq8').addEventListener("click", function () {
  if (playersTurn.textContent === "Player 1's Turn (X)") {
    changeToX(sq8);
  } else if (playersTurn.textContent === "Player 2's Turn (O)") {
    changeToO(sq8);
}      
})

document.querySelector('#sq9').addEventListener("click", function () {
  if (playersTurn.textContent === "Player 1's Turn (X)") {
    changeToX(sq9);
  } else if (playersTurn.textContent === "Player 2's Turn (O)") {
    changeToO(sq9);
}      
})

document.querySelector('#clear').addEventListener('click', function() {
    clearBoard();
})
/*---------------------------FUNCTIONS--------------------------*/

function changeToX(e) {
      if (output.textContent === "Player 1 Wins!" || output.textContent === "Player 2 Wins!") {
      gameEnd();
      return;
    } else if (e.textContent === 'O' || e.textContent === 'X' ) {    
      chooseAnotherBox();
      return;
    } else (playersTurn.textContent === "Player 1's Turn (X)") 
    e.textContent = "X";
    playersTurn.textContent = "Player 2's Turn (O)";
    output.style.color = 'green';
    output.textContent = "Go!";
      playerOneWins();
}

function changeToO(e) {
  if (output.textContent === "Player 1 Wins!" || output.textContent === "Player 2 Wins!") {
    gameEnd();
    return;
  } else if (e.textContent === 'O' || e.textContent === 'X' ) {    
    chooseAnotherBox();
    return;
  } else (playersTurn.textContent === "Player 2's Turn (O)")
  e.textContent = "O"; 
  playersTurn.textContent = "Player 1's Turn (X)";
  output.style.color = 'green';
  output.textContent = "Go!";
    playerTwoWins();
}

function chooseAnotherBox() {
    output.style.color = 'red';
    output.textContent = "Choose a Different Box";
}

function clearBoard() {
    sq1.textContent = " ";
    sq2.textContent = "  ";
    sq3.textContent = "   ";
    sq4.textContent = "    ";
    sq5.textContent = "     ";
    sq6.textContent = "      ";
    sq7.textContent = "       ";
    sq8.textContent = "        ";
    sq9.textContent = "         ";
    playersTurn.textContent = "Player 1's Turn (X)";
    chooseAnotherBox();
    output.style.color = 'green';
    output.textContent = "Let's Begin!";
    gameOver.textContent = ""
}

function gameEnd(){
    gameOver.style.color = "red";
    gameOver.textContent = 'PLEASE RESET THE GAME TO CONTINUE';
    
}

/*--------------------------WINNING CONDITIONS------------------------*/

function playerOneWins() {
    if (sq1.textContent === sq2.textContent && sq2.textContent === sq3.textContent ||
      sq4.textContent === sq5.textContent && sq5.textContent === sq6.textContent ||  
      sq7.textContent === sq8.textContent && sq8.textContent === sq9.textContent ||
      sq1.textContent === sq4.textContent && sq4.textContent === sq7.textContent ||
      sq3.textContent === sq6.textContent && sq6.textContent === sq9.textContent ||
      sq2.textContent === sq5.textContent && sq5.textContent === sq8.textContent ||
      sq3.textContent === sq5.textContent && sq5.textContent === sq7.textContent ||
      sq1.textContent === sq5.textContent && sq5.textContent === sq9.textContent) {
    output.style.color = 'green';
    output.textContent = "Player 1 Wins!";
        } else
        return;
}

function playerTwoWins() {
  if (sq1.textContent === sq2.textContent && sq2.textContent === sq3.textContent ||
      sq4.textContent === sq5.textContent && sq5.textContent === sq6.textContent ||  
      sq7.textContent === sq8.textContent && sq8.textContent === sq9.textContent ||
      sq1.textContent === sq4.textContent && sq4.textContent === sq7.textContent ||
      sq3.textContent === sq6.textContent && sq6.textContent === sq9.textContent ||
      sq2.textContent === sq5.textContent && sq5.textContent === sq8.textContent ||
      sq3.textContent === sq5.textContent && sq5.textContent === sq7.textContent ||
      sq1.textContent === sq5.textContent && sq5.textContent === sq9.textContent) {
  output.style.color = 'green';
  output.textContent = "Player 2 Wins!";
      } else
      return;
}
```
## Functions
| Functions | Description |
| ----------- | ----------- |
| `changeToX(e)` | Changes DIV to X selection. |
| `changeToO(e)` | Changes DIV to O selection. |
| `chooseAnotherBox()` | Tells player to choose another box if box is occupied. |
| `clearBoard()` | Resets the game. |
| `gameEnd()` | Ends the game so you must restart if someone wins. |
| `playerOneWins()` | Check status to see if P1 wins. |
| `playerTwoWins()` | Check status to see if P2 wins. |
