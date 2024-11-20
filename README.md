# techrise-basic-password-login
basic password and login i coded that redirects to any website/place of your choice.
code is below:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Page</title>
    <style>
        
       body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f4f4f9;
        }
        .login-container {
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            border-radius: 10px;
            width: 300px;
        }
        .login-container h2 {
            margin-bottom: 20px;
            text-align: center;
        }
        .form-group {
            margin-bottom: 15px;
        }
        .form-group label {
            display: block;
            margin-bottom: 5px;
        }
        .form-group input {
            width: 100%;
            padding: 8px;
            box-sizing: border-box;
        }
        .login-btn {
            width: 100%;
            padding: 10px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }
        .login-btn:hover {
            background-color: #45a049;
        }
        .error-message {
            color: red;
            text-align: center;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <h2>Login</h2>
        <div class="form-group">
            <label for="username">Username:</label>
            <input type="text" id="username" placeholder="Enter your username">
        </div>
        <div class="form-group">
            <label for="password">Password:</label>
            <input type="password" id="password" placeholder="Enter your password">
        </div>
        <button class="login-btn" onclick="login()">Login</button>
        <div class="error-message" id="error-message"></div>
    </div>

    <script>
        // Hardcoded username-password pairs
        const users = {
            "USER1": "PASSWORD1",
            "USER2": "PASSWORD2",
            "USER3": "PASSWORD3",
            add more if you like.
        };

        // Redirect URL
        const redirectURL = "add the URL of the place this website will go to.";

        function login() {
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            const errorMessage = document.getElementById('error-message');

            // Check if the username exists and the password matches
            if (users[username] && users[username] === password) {
                // Redirect to the target URL
                window.location.href = redirectURL;
            } else {
                // Display error message
                errorMessage.textContent = "Invalid username or password.";
            }
        }
    </script>
</body>
</html>

