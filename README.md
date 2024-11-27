
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sorry na, umuwi ka na baby</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            width: 100vw;
            font-family: Arial, sans-serif;
            background-color: pink; /* Background color set to pink */
            position: relative; /* Allow absolute positioning for buttons */
            margin: 0; /* Remove default margin */
        }
        img {
            width: 30%; /* Adjust the size of the GIFs relative to the viewport */
            max-width: 300px; /* Maximum width for larger screens */
            height: auto;
        }
        button {
            margin: 10px;
            padding: 10px 20px;
            font-size: 2vw; /* Font size relative to viewport width */
            cursor: pointer;
            background-color: black; /* Button background color */
            color: white; /* Button text color */
            border: none;
            border-radius: 5px;
        }
        .no-button {
            background-color: red; /* No button background color */
            color: white; /* No button text color */
            position: absolute; /* Position buttons absolutely */
        }
        h1 {
            font-style: italic; /* Set font style to italic */
            text-align: center; /* Center text */
            font-size: 3vw; /* Font size relative to viewport width */
        }
    </style>
</head>
<body>

    <img id="sadCat" src="https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif" alt="Sad Cat">
    <h1>I’m sorry please forgive me my Love?</h1>
    <button id="yesButton">Yes</button>
    <button id="noButton">No</button>

    <div id="noButtonsContainer"></div>

    <script>
        const yesButton = document.getElementById('yesButton');
        const noButton = document.getElementById('noButton');

        yesButton.addEventListener('click', function() {
            document.body.innerHTML = `
                <img src="https://media1.tenor.com/m/xx3n8cnrnGYAAAAd/nyano-nyano-cat.gif" alt="Gif Image">
                <h1><i>Thank you so much for understanding Baby. I love you with all my heart, body, and soul. I regret my actions and will never let it happen again. My sincere apologies. I love you wifey ko.</i></h1>
            `;
        });

        noButton.addEventListener('click', function() {
            const newNoButton = document.createElement('button');
            newNoButton.textContent = 'No';
            newNoButton.className = 'no-button'; // Add class for styling
            newNoButton.style.left = Math.random() * 80 + 'vw'; // Random horizontal position
            newNoButton.style.top = Math.random() * 80 + 'vh'; // Random vertical position

            newNoButton.addEventListener('click', function() {
                noButtonsContainer.appendChild(newNoButton.cloneNode(true));
                newNoButton.style.left = Math.random() * 80 + 'vw'; // Randomize position again
                newNoButton.style.top = Math.random() * 80 + 'vh'; // Randomize position again
            });

            document.body.appendChild(newNoButton); // Append new button to body
        });
    </script>

</body>
</html>