<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Web Page</title>
    <style>
        /* CSS Styles */
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            margin: 0;
            padding: 0;
        }

        header, footer {
            text-align: center;
            background-color: #333;
            color: white;
            padding: 1em;
        }

        main {
            padding: 20px;
        }

        button {
            padding: 10px 20px;
            margin: 10px;
            background-color: #007BFF;
            color: white;
            border: none;
            cursor: pointer;
        }

        button:hover {
            background-color: #0056b3;
        }

        #new-element {
            background-color: #d3d3d3;
            padding: 10px;
            margin-top: 20px;
            display: none;
        }
    </style>
</head>
<body>

    <header>
        <h1>Welcome to My Interactive Web Page</h1>
    </header>

    <main>
        <!-- Section for changing text content -->
        <section>
            <p id="text-content">This is the original text content.</p>
            <button id="change-text-btn">Change Text</button>
        </section>

        <!-- Section for changing styles -->
        <section>
            <p id="style-paragraph">This text will change style.</p>
            <button id="change-style-btn">Change Style</button>
        </section>

        <!-- Section for toggling an element -->
        <section>
            <button id="toggle-element-btn">Toggle Element</button>
            <div id="new-element">
                <p>This is a new dynamically added element!</p>
            </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 Interactive Web Page</p>
    </footer>

    <script>
        // JavaScript to change the text content dynamically
        document.getElementById('change-text-btn').addEventListener('click', function() {
            document.getElementById('text-content').textContent = 'The text has been updated!';
        });

        // JavaScript to change the CSS styles dynamically
        document.getElementById('change-style-btn').addEventListener('click', function() {
            const paragraph = document.getElementById('style-paragraph');
            paragraph.style.color = 'blue';
            paragraph.style.fontSize = '20px';
            paragraph.style.fontWeight = 'bold';
        });

        // JavaScript to add or remove an element when the button is clicked
        document.getElementById('toggle-element-btn').addEventListener('click', function() {
            const newElement = document.getElementById('new-element');
            if (newElement.style.display === 'none') {
                newElement.style.display = 'block';
            } else {
                newElement.style.display = 'none';
            }
        });
    </script>
</body>
</html>
