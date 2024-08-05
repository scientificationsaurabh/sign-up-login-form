<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sign Up and Log In</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f0f4f8;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .form-container {
            background: #fff;
            padding: 20px 40px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        h1 {
            margin-bottom: 10px;
            color: #333;
        }

        p {
            color: #666;
        }

        form {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        input {
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 16px;
        }

        button {
            padding: 10px;
            border: none;
            border-radius: 5px;
            background: #007bff;
            color: #fff;
            font-size: 16px;
            cursor: pointer;
        }

        button:hover {
            background: #0056b3;
        }

        a {
            color: #007bff;
            text-decoration: none;
        }

        a:hover {
            text-decoration: underline;
        }

        .form-box {
            display: none;
        }
        
        .form-box.active {
            display: block;
        }
    </style>
</head>
<body>
    <div class="form-container" id="form-container">
        <!-- Registration Form -->
        <div class="form-box active" id="signup-box">
            <h1>Sign Up</h1>
            <p>Quick and easy</p>
            <form id="signup-form">
                <input type="text" id="signup-name" placeholder="Enter your name" required>
                <input type="email" id="signup-email" placeholder="Enter your email" required>
                <input type="password" id="signup-password" placeholder="Enter your password" required>
                <button type="submit">Sign up</button>
            </form>
            <p>Already have an account? <a href="#" id="show-login">Log in</a></p>
        </div>

        <!-- Login Form -->
        <div class="form-box" id="login-box">
            <h1>Smart Login System</h1>
            <form id="login-form">
                <input type="email" id="login-email" placeholder="Enter your email" required>
                <input type="password" id="login-password" placeholder="Enter your password" required>
                <button type="submit">Log in</button>
            </form>
            <p>Don’t have an account? <a href="#" id="show-signup">Sign up</a></p>
        </div>
    </div>

    <script>
        document.getElementById('show-login').addEventListener('click', function(event) {
            event.preventDefault();
            document.getElementById('signup-box').classList.remove('active');
            document.getElementById('login-box').classList.add('active');
        });

        document.getElementById('show-signup').addEventListener('click', function(event) {
            event.preventDefault();
            document.getElementById('login-box').classList.remove('active');
            document.getElementById('signup-box').classList.add('active');
        });

        window.onload = function() {
            document.getElementById('signup-box').classList.add('active');
        };
    </script>
</body>
</html>

