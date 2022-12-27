<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3D Card Flip</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Fredoka+One&display=swap" rel="stylesheet"> 
    <style>
        * {
            margin: 0;
            padding: 0;
            font-family: 'Fredoka One', cursive;
        }

        body {
            background-color: #383838;
        }

        section {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100%;
            height: 100vh;
        }

        aside.card {
            width: 300px;
            height: 200px;
            position: relative;
            perspective: 600px;
        }


        aside.card div.front,
        aside.card div.back {
            position: absolute;
            top: 0;
            width: 100%;
            height: 100%;
            transform-style: preserve-3d;
            backface-visibility: hidden;
            transition: 0.5s all ease-in-out;
            border-radius: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 40px;
            color: #fff;
            text-shadow: 0 2px 0 #777777;
        }

        aside.card div.front {
            background-color: #e24f24;
            z-index: 1000;
            transform: rotateX(0deg);
        }

        aside.card div.back {
            background-color: #006cb6;
            z-index: 900;
            transform: rotateX(-180deg);
        }

        aside.card:hover div.front {
            z-index: 900;
            transform: rotateX(180deg);
        }

        aside.card:hover div.back {
            z-index: 1000;
            transform: rotateX(0deg);
        }
        
    </style>
</head>
<body>
    <section>
        <aside class="card">
            <div class="front">
                HTML
            </div>
            <div class="back">
                CSS
            </div>
        </aside>
    </section>
</body>
</html>
