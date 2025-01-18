<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title id="title"></title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
    <script>
        // Fetch JSON content dynamically
        fetch('/content/index.json')
            .then(response => response.json())
            .then(data => {
                document.getElementById('title').innerText = data.title;
                document.getElementById('heading').innerText = data.heading;
                document.getElementById('description').innerText = data.description;
                document.getElementById('cta').innerText = data.cta_text;
                document.getElementById('cta').href = data.cta_link;
            });
    </script>
    <style>
        /* Same CSS as before */
    </style>
</head>
<body>
    <div class="container">
        <h1 id="heading"></h1>
        <p id="description"></p>
        <div class="loader"></div>
        <div class="cta">
            <a id="cta" class="button" href="#"></a>
        </div>
    </div>
</body>
</html>
