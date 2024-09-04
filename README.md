<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WebPage with Brython</title>
    <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/brython@3.9.5/brython.min.js"></script>
</head>
<style>
    body {
        background-color: #121212;
        color: #ffffff;
        font-family: 'Arial', sans-serif;
    }

    a {
        color: #bb86fc;
        text-decoration: none;
    }

    a:hover {
        text-decoration: underline;
    }

    button {
        background-color: #1f1f1f;
        color: #ffffff;
        border: 1px solid #bb86fc;
        padding: 10px 15px;
        cursor: pointer;
        font-family: 'Arial', sans-serif;
        transition: background-color 0.3s, color 0.3s;
    }

    button:hover {
        background-color: #bb86fc;
        color: #121212;
    }

    h1, h2, h3 {
        color: #ffffff;
        font-family: 'Arial', sans-serif;
    }

    p {
        color: #e0e0e0;
        font-family: 'Arial', sans-serif;
    }
</style>


<body onload="brython()">

<h1>Example of using Brython</h1>


<script type="text/python">
    from browser import document

    def greet(event):
        document["output"].text = "Hello World!!"
    def greet_2(event):
        document["output"].text = ""



    document["my_button"].bind("click", greet)
    document["my_button_2"].bind("click", greet_2)
</script>

<button id="my_button">+</button>
<button id="my_button_2">-</button>
<p id="output"></p>

</body>
</html>
