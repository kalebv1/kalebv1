<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Let Me Court You Again</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f9f9f9;
            color: #333;
            text-align: center;
            padding: 50px;
        }

        .container {
            background: white;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            padding: 20px;
        }

        button {
            margin: 10px;
            padding: 10px 20px;
            font-size: 16px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        #yes-button {
            background-color: #28a745;
            color: white;
        }

        #no-button {
            background-color: #dc3545;
            color: white;
        }

        input {
            padding: 10px;
            margin-top: 10px;
            font-size: 16px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        #submit-activity {
            background-color: #007bff;
            color: white;
        }

        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Let Me Court You Again</h1>
        <p id="question">Would you like to go out with me?</p>
        <button id="yes-button">Yes</button>
        <button id="no-button">No</button>
        <div id="response" class="hidden"></div>
        <div id="next-question" class="hidden">
            <p>What do you enjoy doing on a date?</p>
            <input type="text" id="activity" placeholder="e.g., Dinner, Movie">
            <button id="submit-activity">Submit</button>
        </div>
    </div>
    <script>
        document.getElementById('yes-button').addEventListener('click', function() {
            document.getElementById('response').innerText = 'Thank you, I love you!';
            document.getElementById('response').classList.remove('hidden');
            document.getElementById('next-question').classList.add('hidden');
            document.getElementById('question').classList.add('hidden');
            document.getElementById('yes-button').classList.add('hidden');
            document.getElementById('no-button').classList.add('hidden');
        });

        document.getElementById('no-button').addEventListener('click', function() {
            document.getElementById('response').innerText = 'That’s okay, maybe another time!';
            document.getElementById('response').classList.remove('hidden');
        });

        document.getElementById('submit-activity').addEventListener('click', function() {
            const activity = document.getElementById('activity').value;
            document.getElementById('response').innerText = `Sounds fun! A ${activity} date would be great!`;
            document.getElementById('response').classList.remove('hidden');
            document.getElementById('next-question').classList.add('hidden');
        });
    </script>
</body>
</html>
