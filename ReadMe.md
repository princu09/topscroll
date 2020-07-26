## Top Scroll CSS Layout Free Source Code By NorthFox Developers

#### Join Our Telegram Channel [ProgHub09](http://t.me/ProgHub09) and Also Download Our App.

![Video Here](TopScroll.gif)

#### HTML File

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Scroll Bar</title>
    <link rel="stylesheet" href="style.css">
    <link rel="shortcut icon" href="https://princu09.github.io/nfwebbuilder/img/logo.png" type="image/png">
</head>

<body>
    <div id="progressbar"></div>
    <div id="scrollPath"></div>
    <section>
        <h2>Creative Top Scroll Bar</h2>
        <p>&emsp;&emsp;&emsp; Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis earum, error totam illo mollitia repellendus labore qui. Quis nostrum delectus error ab deserunt commodi nisi similique harum quidem consequatur, beatae molestias
        
        <!-- Other Lorem Text -->

        </p>
    </section>

    <script>
        let progress = document.getElementById('progressbar');
        let totalWidth = document.body.scrollHeight - window.innerHeight;

        window.onscroll = function() {
            let progressWidth = (window.pageYOffset / totalWidth) * 100;
            progress.style.width = progressWidth + "%";
        }
    </script>
</body>

</html>
```

#### CSS File

```
* {
    margin: 0;
    padding: 0;
    font-family: cursive;
}

body {
    width: 100%;
    height: 100vh;
    color: #fff;
}

section {
    padding: 50px;
    background: #000;
}

section h2 {
    font-size: 2.5em;
    padding: 20px;
    text-align: center;
}

section p {
    font-size: 1.2em;
}

::-webkit-scrollbar {
    width: 0;
}

#scrollPath {
    position: fixed;
    top: 0;
    width: 100%;
    height: 5px;
    background: rgba(255, 255, 255, 0.05);
}

#progressbar {
    position: fixed;
    top: 0;
    height: 6px;
    background: linear-gradient(to left, #008aff, #00ffe7);
    animation: animate 5s linear infinite;
}

@keyframes animate {
    0%,
    100% {
        filter: hue-rotate(0deg);
    }
    50% {
        filter: hue-rotate(360deg);
    }
}

#progressbar::before {
    content: '';
    position: absolute;
    top: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to left, #008aff, #00ffe7);
    filter: blur(10px);
}

#progressbar::after {
    content: '';
    position: absolute;
    top: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to left, #008aff, #00ffe7);
    filter: blur(30px);
}

@media screen and (max-width:400px) {
    section h2 {
        font-size: 1.5em;
        padding: 20px;
        text-align: center;
    }
    section p {
        font-size: 1em;
    }
    section {
        padding: 20px;
        background: #000;
    }
}
```