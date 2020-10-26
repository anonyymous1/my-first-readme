# My First README

Repo explaining README.md

```Javascript
const handleWin = (letter) => {
  gameIsLive = false;
  if (letter === "x") {
    statusDiv.innerHTML = `${letterToSymbol(letter)} has won!`;
  } else {
    statusDiv.innerHTML = `<span>${letterToSymbol(letter)} has won!</span>`;
  }
};
```
##Steps to install Tic Tac Toe to computer
1. Go to [Repo] (https://github.com/SEI-ATL/tic-tac-toe)
2. `Fork` page.
3. `Clone` code.
4. Open iTerm2 .
5. Type `git clone https://github.com/SEI-ATL/tic-tac-toe`
6.

```CSS
.grid {
    background-color: salmon;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(3, 1fr);
    gap: 15px;
    margin-top: 50px;
}
```

```HTML
<div class="grid">
    <div class="box" id="box-1"></div>
    <div class="box" id="box-2"></div>
    <div class="box" id="box-3"></div>
    <div class="box" id="box-4"></div>
    <div class="box" id="box-5"></div>
    <div class="box" id="box-6"></div>
    <div class="box" id="box-7"></div>
    <div class="box" id="box-8"></div>
    <div class="box" id="box-9"></div>
</div>
```

| Functions | Description |
| ----------- | ----------- |
| `handleWin()` | Handle the win of each player |
| `checkGameStatus()` | Check status after each move. |