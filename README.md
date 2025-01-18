<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Embedded Browser</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            width: 100%;
        }

        iframe {
            border: none;
            width: 100%;
            height: 100%;
        }

        .header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: #333;
            color: white;
            padding: 10px;
            font-size: 18px;
            z-index: 1000;
        }

        .iframe-container {
            margin-top: 50px;
            height: calc(100% - 50px);
        }
    </style>
</head>
<body>
    <div class="header">
        Embedded Browser (Incognito Simulation)
    </div>
    <div class="iframe-container">
        <iframe src="https://www.example.com" title="Embedded Website"></iframe>
    </div>
</body>
</html>
