<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Landing Page</title>
    <style>
        *{
            
        }
        body {
            margin: 0;
            font-family: Arial, sans-serif;
        }
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background: transparent;
            display: flex;
            justify-content: space-around;
            align-items: center;
            padding: 15px;
            transition: background 0.3s ease-in-out;
        }
        .navbar.scrolled {
            background: #333;
        }
        .navbar a {
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            transition: color 0.3s;
        }
        .navbar a:hover {
            color: yellow;
        }
        .hero {
            height: 100vh;
            background: url('https://source.unsplash.com/random/1600x900') no-repeat center center/cover;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 2em;
        }
        .content {
            height: 100vh;
            background: white;
            text-align: center;
            padding: 50px;
        }
    </style>
</head>
<body>
    <nav class="navbar" id="navbar">
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Services</a>
        <a href="#">Contact</a>
    </nav>
    <div class="hero">
        Welcome to Our Website
    </div>
    <div class="content">
        <h2>About Us</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque sit amet.</p>
    </div>
    <script>
        window.addEventListener('scroll', function() {
            let navbar = document.getElementById('navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });
    </script>
</body>
</html>
