<center>umuwi ka na baby</center>
<html lang="en"> 
<head> 
    <meta charset="UTF-8"> 
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
    <title>Sorry na, umuwi ka na Baby</title> 
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            width: 100vw;
            font-family: 'Times New Roman', Times, serif; /* Ensures the font is applied */
            background-color: pink; 
            position: relative; 
            margin: 0; /* Reset default margin */
            padding: 0; /* Reset default padding */
        }
        img {
            width: 30%; 
            max-width: 300px; 
            height: auto;
            display: block; /* Ensures the image behaves as a block element */
            margin: 0 auto; /* Centers the image */
        }
        button {
            margin: 10px;
            padding: 10px 20px;
            font-size: 2vw; 
            cursor: pointer;
            background-color: black; 
            color: white; 
            border: none;
            border-radius: 5px;
        }
        .no-button {
            background-color: red; 
            color: white; 
            position: absolute; 
        }
        h1 {
            font-style: italic; 
            text-align: center; 
            font-size: 3vw; 
            margin: 10px 0; /* Add margin to the heading */
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
        const noButtonsContainer = document.getElementById('noButtonsContainer'); // Make sure this is defined

        yesButton.addEventListener('click', function() {
            document.body.innerHTML = `
                <img src="https://media1.tenor.com/m/xx3n8cnrnGYAAAAd/nyano-nyano-cat.gif" alt="Gif Image" style="display: block; margin: 0 auto;">
                <h1><i>Thank you so much for understanding Baby. I love you with all my heart, body, and soul. I regret my actions and will never let it happen again. My sincere apologies, I hope you're doing well right now. I love you wifey ko.</i></h1>
            `;
        });

        noButton.addEventListener('click', function() {
            const newNoButton = document.createElement('button');
            newNoButton.textContent = 'No';
            newNoButton.className = 'no-button'; 
            newNoButton.style.left = Math.random() * 80 + 'vw'; 
            newNoButton.style.top = Math.random() * 80 + 'vh'; 

            newNoButton.addEventListener('click', function() {
                noButtonsContainer.appendChild(newNoButton.cloneNode(true));
                newNoButton.style.left = Math.random() * 80 + 'vw'; 
                newNoButton.style.top = Math.random() * 80 + 'vh'; 
            });

            document.body.appendChild(newNoButton); 
        });
    </script> 
</body>
</html>
