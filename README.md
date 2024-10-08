login.html

<!DOCTYPE html>
<html>
<head>
    <title>Login</title>
     <style>
        body {
            font-family: Arial, sans-serif;
            background: url("./bg.png") ;
            
            background-size: cover;
            background-position:center;
            overflow: hidden;
            margin: 0;
            padding: 0;
        }
        .container {
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .rectangle-cylinder-box {
            background: #3498db; /* Blue Color */
            width: 600px;
            height: 400px;
            border-radius: 20px;
            position: relative;
             background:transparent;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            display: flex;
            flex-direction: column; /* Change flex-direction to column */
            justify-content: center; /* Align items vertically */
            align-items: center; /* Align items horizontally */
            animation: shimmer 2s infinite;
        }

        /* Login Form Styles */
        .login-form {
            width: 80%;
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 10px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
             backdrop-filter: blur(16px) saturate(185%);
    -webkit-backdrop-filter: blur(16px) saturate(185%);
    background-color: rgba(255, 255, 255, 0.21);
    border-radius: 12px;
    padding:30px;
    border: 1px solid rgba(209, 213, 219, 0.3);

        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            font-weight: bold;
        }
        input[type="text"], input[type="password"] {
            width: 100%;
            margin-top:10px;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 16px;
            outline:none;
            border:none;
        }
        .submit-button {
            background-color: #007bff;
            color: #fff;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
            margin-bottom:20px;
            margin-top:20px;
                  transition:all 0.3s ease

        }

        .submit-button:hover {
            background-color: #0056b3;
            outline: 3px solid #007bff;
        }
        /* Bubbles Animation */
        @keyframes bubble {
            0%, 100% {
                transform: translateY(100vh) translateX(100vw);
                opacity: 0;
            }
            50% {
                transform: translateY(-100px) translateX(-100px);
                opacity: 1;
            }
        }
        .bubble {
            position: absolute;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            animation: bubble 8s infinite;
            transform-origin: center;
        }
        .bubble.brown {
            background-color: #8B4513; /* Brown Color */
            animation-delay: -1s;
        }
        .bubble.blue {
            background-color: #1E90FF; /* Blue Color */
            animation-delay: -2s;
        }
        .bubble.green {
            background-color: #00FF7F; /* Green Color */
            animation-delay: -3s;
        }
        .bubble.purple {
            background-color: #8A2BE2; /* Purple Color */
            animation-delay: -4s;
        }
        .flash-messages {
            list-style: none;
            padding: 0;
            margin-top: 10px;
        }
        .flash-messages li {
            background-color: #f8d7da;
            color: #721c24; /* Change text color to red */
            padding: 10px;
            border-radius: 5px;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="rectangle-cylinder-box">
            <div class="cylinder"></div>
            <div class="login-form">
                <h1 class="login-header">Login</h1>
                <!-- Flash Messages inside the same container, below the header -->
                <ul class="flash-messages">
                    
                </ul>
                <p>Please enter your registered credentials:</p>
                <form method="POST" action="/login">
                    <div class="form-group">
                        <label for="username">Username</label>
                        <input type="text" name="username" class="form-control" autofocus="true" autocomplete="off">
                    </div>
                    <div class="form-group">
                        <label for="password">Password</label>
                        <input type="password" name="password" class="form-control">
                    </div>
                    <div class="form-group">
                        <button class="submit-button" type="submit">Login</button>
                    </div>
                </form>
                <a class="register-link" href="./register.html"> <p>Don't have an account?</p> Register here</a>
            </div>
        </div>
    </div>
    <!-- Bubble Elements -->
    <div class="bubble brown" style="top: 30vh; left: 20vw;"></div>
    <div class="bubble blue" style="top: 50vh; left: 60vw;"></div>
    <div class="bubble green" style="top: 70vh; left: 40vw;"></div>
</body>
</html>



register.html

<!DOCTYPE html>
<html>
<head>
    <title>Register</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: url(./bg.png);
            background-size: cover;
            box-shadow: rgba(17, 17, 26, 0.1) 0px 4px 16px, rgba(17, 17, 26, 0.1) 0px 8px 24px, rgba(17, 17, 26, 0.1) 0px 16px 56px;
            overflow: hidden;
            margin: 0;
            padding: 0;
        }
        .container {
            position: relative;
            display: flex;

            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .rectangle-cylinder-box {

          padding:80px;
            border-radius: 1000%;
            position: relative;
          backdrop-filter: blur(16px) saturate(185%);
    -webkit-backdrop-filter: blur(16px) saturate(185%);
    background-color: rgba(255, 255, 255, 0.21);
    border-radius: 12px;
    border: 1px solid rgba(209, 213, 219, 0.3);

            display: flex;
            flex-direction: column; /* Change flex-direction to column */
            justify-content: center; /* Align items vertically */
            align-items: center; /* Align items horizontally */
            animation: shimmer 2s infinite;
        }

        /* Login Form Styles */
        .login-form {
            width: 60px;
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 10px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            font-weight: bold;
        }
        input[type="text"], input[type="password"] {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            outline:none;
            border:none;
            font-size: 16px;
            margin-top:0px;
            box-shadow: rgba(0, 0, 0, 0.15) 0px 15px 25px, rgba(0, 0, 0, 0.05) 0px 5px 10px;
        }
        .submit-button {

            background-color: #007bff;
            color: #fff;
            border: none;
            text-decoration:none;
            padding: 10px 20px;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
            margin-bottom:0px;
            margin-top:0px;
             transition:all 0.3s ease

        }

        .submit-button:hover {
            background-color: #0056b3;
            outline: 3px solid #007bff;
        }
        /* Bubbles Animation */
        @keyframes bubble {
            0%, 100% {
                transform: translateY(100vh) translateX(100vw);
                opacity: 0;
            }
            50% {
                transform: translateY(-100px) translateX(-100px);
                opacity: 1;
            }
        }
        .bubble {
            position: absolute;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            animation: bubble 8s infinite;
            transform-origin: center;
        }
        .bubble.brown {
            background-color: #8B4513; /* Brown Color */
            animation-delay: -1s;
        }
        .bubble.blue {
            background-color: #1E90FF; /* Blue Color */
            animation-delay: -2s;
        }
        .bubble.green {
            background-color: #00FF7F; /* Green Color */
            animation-delay: -3s;
        }
        .bubble.purple {
            background-color: #8A2BE2; /* Purple Color */
            animation-delay: -4s;
        }
        .flash-messages {
            list-style: none;
            padding: 0;
            margin-top: 10px;
        }
        .flash-messages li {
            background-color: #f8d7da;
            color: #721c24; /* Change text color to red */
            padding: 10px;
            border-radius: 5px;
            margin-top: 10px;
        }

    </style>
</head>
<body>
    <div class="container">
        <div class="rectangle-cylinder-box">
            <div class="cylinder"></div>
            <div class="registration-form">
                <h1 class="register-header">Register</h1>
                <!-- Flash Messages inside the same container, below the header -->
                
                <form method="POST" action="/register">
    
    <div class="form-group">
        <label for="username">Username</label>
        <input type="text" name="phone_number" class="form-control">
    </div>
    <!-- Corrected field name for Date of Birth -->

    <div class="form-group">
        <label for="phone_number">Phone Number</label>
        <input type="text" name="phone_number" class="form-control">
    </div>
    <div class="form-group">
        <label for="email">Email</label>
        <input type="text" name="email" class="form-control">
    </div>
                        <div class="form-group">
        <label for="age">Age</label>
        <input type="text" name="age" class="form-control">
    </div>
                     <div class="form-group">
        <label for="gender">Gender</label>
        <input type="text" name="gender" class="form-control">
    </div>
                     <div class="form-group">
        <label for="address">Address</label>
        <input type="text" name="address" class="form-control">
    </div>


    <div class="form-group">
        <label for="password">Password</label>
        <input type="password" name="password" class="form-control">
    </div>
    <div class="form-group">
        <button class="submit-button" type="submit">Register</button>

    </div>
   <a class="login-link" href="./login.html">Already have an account? Login here</a>
</form>

            </div>
        </div>
    </div>
    <!-- Bubble Elements -->
    <div class="bubble brown" style="top: 30vh; left: 20vw;"></div>
    <div class="bubble blue" style="top: 50vh; left: 60vw;"></div>
    <div class="bubble green" style="top: 70vh; left: 40vw;"></div>
</body>
</html>
