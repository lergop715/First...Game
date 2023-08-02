# First...Game

Created these before sophmore year, and yes I was self taught.
I promise I'm a ton better.

Html code

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Guess the Number Game</title>
    <link rel="stylesheet" href="Guess.css">
</head>
<body>
    <h1>Guess the Number Game</h1>
    <p>Try to guess the random number between 1 and 100:</p>
    <input type="number" id="userGuess">
    <button onclick="checkGuess()">Submit</button>
    <p id="feedback"></p>

    <script src="Guess.js"></script>
</body>
</html>

CSS

body {
    font-family: Arial, sans-serif;
    text-align: center;
    padding: 20px;
}

h1 {
    margin-bottom: 20px;
}

p {
    margin-bottom: 10px;
}

input {
    width: 100px;
    padding: 5px;
}

button {
    padding: 5px 10px;
    background-color: #007BFF;
    color: #fff;
    border: none;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}

JS


const randomNumber = Math.floor(Math.random() * 100) + 1;


function checkGuess() {
    const userGuess = parseInt(document.getElementById('userGuess').value);

    if (isNaN(userGuess)) {
        document.getElementById('feedback').innerText = 'Please enter a valid number.';
    } else if (userGuess < 1 || userGuess > 100) {
        document.getElementById('feedback').innerText = 'Please enter a number between 1 and 100.';
    } else if (userGuess === randomNumber) {
        document.getElementById('feedback').innerText = 'Congratulations! You guessed the correct number!';
    } else if (userGuess < randomNumber) {
        document.getElementById('feedback').innerText = 'Try again. The correct number is higher.';
    } else {
        document.getElementById('feedback').innerText = 'Try again. The correct number is lower.';
    }
}

Enjoy

Css
