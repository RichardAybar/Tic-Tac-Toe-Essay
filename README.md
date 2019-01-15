# Tic-Tac-Toe-Essay

	My mission was to create a tic tac toe game in Javascript, using html, css and jquery. To start off we will need to set up our front end and back end. In this project we used github pages and heroku to host our app. After our setup is complete we can start with html in our text editor. Firt thing to do is create a board for our game, I used a table but there are many other options such as bootstrap or flexbox. We will need to create a 3 by 3 grid. After you have a grid we will target the inner html and populate with a token, in this case "X" or "O".


```javascript
    if (movesMade % 2 === 0) {
      currentPlayer = playerOne
    } else {
      currentPlayer = playerTwo
    }
```

	I was not completely sure how to approach the game logic at first. Once I had an array setup for my grid I implemented some game logic to check for all 8 different win possibilities. I did this by checking to see if the "value" or player token of a particular tile in my grid was equal to other corresponding tiles that would cause a win. For example I checked to see if the top row was all the same by comparing the values of all those positions against eachother. When creating my grid I used an array with 3 empty arrays inside, filled with 3 empty values, like so:


```javascript
const grid = [
    [' ', ' ', ' '],
    [' ', ' ', ' '],
    [' ', ' ', ' ']
];
```


	Using this setup I can form columns and rows that can be called using grid[0][0], grid [0][1] and so on. This lets me pinpoint each tile and check it against other tiles, e.g.
	
```javascript
      for (let a = 0; a < 3; a++) {
        // check for win, horizontal
        if (grid[0][0] !== ' ' &&
        grid[0][0] === grid[0][1] &&
        grid[0][0] === grid[0][2]) {
          return grid[0][0]
}
```


	Using the above inside a function will check for a horizontal win. We can put this code inside a function that checks for a win, as well as checking for every other possible win. After making a functioning board that checks for wins, I needed to implement logic to end game and not allow players to click anymore. It was also neccessary to add a fucntion that checks for a draw. This would consist of checking that all values on grid are taken and no Win requirements have been met.

	I used JQuery to target the tiles in my array by their class that I gave them in HTML. In this project we used AJAX calls to make requests to the API. At first this was diffucult , being it was my first time interacting with an API. After practice and repetiition I was able to recognize the patterns and using AJAX cals became easier. These interactions are what would actually log and register that a move has been on the server side which will be represented on the web page, causing the game to function properly.
