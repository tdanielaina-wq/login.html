<!DOCTYPE html>
<html>
<head>
  <title>Login Form</title>
   <style>
body {
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #f2f2f2;
            font-family: Arial, sans-serif;
        }

 loginbox {
            width: 350px;
            padding: 20px;
            background: white;
            border: 2px solid #ddd;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.2);
        }

h2 {
            text-align: center;
            color: black;
        }

label {
            display: block;
            margin-top: 10px;
            margin-bottom: 5px;
            color: black;
            font-weight: bold;
        }

input {
            width: 100%;
            padding: 10px;
            border: 1px solid #999;
            border-radius: 5px;
            box-sizing: border-box;
        }

button {
            width: 100%;
            margin-top: 15px;
            padding: 10px;
            background-color: blue;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

button:hover {
            background-color: darkblue;
        }

        #message {
            text-align: center;
            margin-top: 10px;
            font-weight: bold;
        }
    </style>
</head>
<body>

<div class="loginbox">
    <h2>Login Form</h2>

    <label>Username</label>
    <input type="text" id="username">

    <label>Password</label>
    <input type="password" id="password">

    <button onclick="login()">Login</button>

    <p id="message"></p>
</div>

<script>
function login() {
    let username = document.getElementById("username").value;
    let password = document.getElementById("password").value;

    if(username === "admin" && password === "12345") {
        document.getElementById("message").style.color = "green";
        document.getElementById("message").innerHTML = "Login Successful!";
    } else {
        document.getElementById("message").style.color = "red";
        document.getElementById("message").innerHTML = "Invalid Username or Password!";
    }
}
</script>

</body>
</html>
