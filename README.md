<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
        }

        .container {
            display: grid;
            grid-template-areas:
                "header"
                "main"
                "footer";
            grid-gap: 10px;
            padding: 10px;
        }

        .header {
            grid-area: header;
            background-color: lightgreen;
            text-align: center;
            padding: 20px;
        }

        .main {
            grid-area: main;
            display: flex;
            gap: 10px;
        }

        .main > div {
            flex: 1;
            text-align: center;
            padding: 20px;
            background-color: lightblue;
        }

        .footer {
            grid-area: footer;
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 10px;
        }

        .footer > div {
            text-align: center;
            padding: 20px;
            background-color: lightgray;
        }

        /* media query when width less than 480px */
        @media (max-width: 480px) {
            .main {
                flex-direction: column;
            }

            .footer {
                grid-template-columns: repeat(2, 1fr);
                gap: 10px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">Header</div>
        <div class="main">
            <div class="left">Left</div>
            <div class="center">Center</div>
            <div class="right">Right</div>
        </div>
        <div class="footer">
            <div>Footer 1</div>
            <div>Footer 2</div>
            <div>Footer 3</div>
            <div>Footer 4</div>
        </div>
    </div>
</body>
</html>
