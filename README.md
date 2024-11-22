<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Change your Mood</title>
</head>
<style>
    @import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');
    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: "Roboto", sans-serif;
  font-weight: 400;
    }

    body{
        background-color: #222;
        transition: 1s;
    }

    .main{
        height: 100vh;
        width: 100%;
        
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .container{
        width: 30rem;
        background-color: #fff;
        padding: 10px;
        border-radius: 10px;
        font-size: 40px;
        text-align: center;
    }

    button{
        font-size: 2rem;
        width: 100%;
        background-color: #222;
        color: #fff;
        border-radius: 5px;
        cursor: pointer;
        margin-top: 14px;
    }
</style>
<body>
    <div class="main">
        <div class="container">
   <h2 id="color-code">#222</h2>
    <button id="btn">Click ME</button>
</div>
</div>

<script>
    function getColor(){
        const randomNumber = Math.floor(Math.random() * 16777215);
        const randomCode = "#"  + randomNumber.toString(16);
        document.body.style.backgroundColor = randomCode;
        document.getElementById("color-code").innerText = randomCode;
    }

    document.getElementById("btn").addEventListener("click" , getColor);
</script>
</body>
</html>
