<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>M.S.M Login & Register</title>

<style>
    body {
        margin: 0;
        padding: 0;
        background: black;
        font-family: Arial, sans-serif;
        color: white;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .container {
        width: 380px;
        background: #111;
        padding: 30px;
        border-radius: 10px;
        box-shadow: 0 0 15px red;
    }

    h2 {
        text-align: center;
        color: red;
        margin-bottom: 20px;
    }

    label { font-size: 14px; }
    
    input {
        width: 100%;
        padding: 12px;
        margin: 8px 0 20px;
        background: #000;
        border: 2px solid red;
        border-radius: 5px;
        color: white;
        font-size: 15px;
    }

    .btn {
        width: 100%;
        padding: 12px;
        background: red;
        border: none;
        border-radius: 5px;
        color: black;
        font-weight: bold;
        font-size: 16px;
        cursor: pointer;
    }
    .btn:hover { background: #ff4d4d; }

    .switch {
        text-align: center;
        margin-top: 15px;
    }
    .switch a {
        color: red;
        cursor: pointer;
        text-decoration: none;
    }

    #register { display: none; }
</style>

<script>
    function showLogin() {
        document.getElementById("login").style.display = "block";
        document.getElementById("register").style.display = "none";
    }

    function showRegister() {
        document.getElementById("login").style.display = "none";
        document.getElementById("register").style.display = "block";
    }

    function loginNow() {
        let user = document.getElementById("username").value;
        let pass = document.getElementById("password").value;

        if (user === "M.Saim" && pass === "MAJOKA") {
            window.location.href = "https://name240.github.io/M.SaimMajoka.../";
        } else {
            alert("? Wrong Username or Password!");
        }
    }
</script>

</head>
<body>

<div class="container">

    <!-- LOGIN FORM -->
    <div id="login">
        <h2>M.S.M Login</h2>

        <label>Username</label>
        <input type="text" id="username" placeholder="Enter Username">

        <label>Password</label>
        <input type="password" id="password" placeholder="Enter Password">

        <button class="btn" onclick="loginNow()">Login</button>

        <div class="switch">
            Don’t have an account? <a onclick="showRegister()">Register</a>
        </div>
    </div>

    <!-- REGISTER FORM -->
    <div id="register">
        <h2>M.S.M Register</h2>

        <label>Create Username</label>
        <input type="text" placeholder="Create Username">

        <label>Email</label>
        <input type="email" placeholder="Enter Email">

        <label>Create Password</label>
        <input type="password" placeholder="Create Password">

        <button class="btn">Register</button>

        <div class="switch">
            Already have an account? <a onclick="showLogin()">Login</a>
        </div>
    </div>

</div>

</body>
</html>
