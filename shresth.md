###SHRESTH SHARMA
-PHOTO:https://www.instagram.com/p/CXf0UzgFMkz/
-LOCATION: INDIA
-GITHUB:https://github.com/dextersherry


<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Counter</title>

    <!--! Style Sheet -->
    <link rel="stylesheet" href="app.css">

    <!-- ! Font link -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+SC:wght@700&family=Staatliches&display=swap" rel="stylesheet">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+SC:wght@700&family=Staatliches&display=swap" rel="stylesheet">
</head>


<body>
    <div class="container">
        <h1>
            Counter
        </h1>
        <span id="value">0</span>
        <div class="button-container">
            <button class="btn decrease">decrease</button>
            <button class="btn reset">reset</button>
            <button class="btn increase">increase</button>
        </div>
    </div>


    <!--!Java Script  -->
    <script src="app.js"></script>
</body>

</html>

body {
    background-image: repeating-linear-gradient(to right, #dee2e6, #e5e5e5 1%);
}

.container {
    padding-top: 100px;
}

h1 {
    display: flex;
    justify-content: center;
    font-family: 'Cormorant SC', serif;
    font-family: 'Staatliches', cursive;
    text-transform: capitalize;
    margin-bottom: 20px;
    /* font-family: monospace; */
    font-size: 468.75%;
}

span {
    display: flex;
    justify-content: center;
    font-size: 562.5%;
}

.button-container {
    display: flex;
    justify-content: center;
    margin: 20px;
}

.btn {
    width: 10%;
    margin: 5px;
    border: 3px solid black;
    text-transform: uppercase;
    font-size: large;
    font-family: 'Cormorant SC', serif;
    font-family: 'Staatliches', cursive;
    border-radius: 5px;
    padding-left: 10px;
    padding-right: 10px;
    transition-duration: 0.4s;
}

.btn:hover {
    background-color: #d3d3d3;
}

@media(max-width:800px) {
    .button-container {
        flex-direction: column;
    }
    .btn {
        margin: auto;
        margin-top: 10px;
        width: 40%;
    }
}

// * set initial count

let count = 0;

const value = document.querySelector('#value');
const btns = document.querySelectorAll(".btn");



btns.forEach(function(btn) {
    btn.addEventListener('click', function(e) {
        const styles = (e.currentTarget.classList);
        if (styles.contains('decrease')) {
            count--;
        } else if (styles.contains('increase')) {
            count++;
        }
        else {
            count = 0;
        }

        if (count > 0) {
            value.style.color = "green";
        }
        if (count < 0) {
            value.style.color = "red";

        }
        if (count === 0) {
            value.style.color = "black";
        }

        value.textContent = count;

    });
});
