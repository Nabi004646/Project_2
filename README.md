<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Coders and Programmers - Project 2</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');

  /* Root styles */
  body {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #ff4444, #ff0000);
    color: black;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    flex-direction: column;
    text-align: center;
    padding: 20px;
  }

  /* Container */
  .container {
    max-width: 600px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 25px;
    padding: 40px 30px;
    box-shadow: 0 0 30px rgba(255, 0, 0, 0.5);
    animation: glow 3s ease-in-out infinite alternate;
  }

  /* Glow animation for container */
  @keyframes glow {
    0% {
      box-shadow: 0 0 15px rgba(255, 0, 0, 0.4);
    }
    100% {
      box-shadow: 0 0 30px rgba(255, 69, 0, 0.8);
    }
  }

  h1 {
    font-size: 2.8rem;
    margin-bottom: 0.4em;
    letter-spacing: 2px;
    animation: slideDown 1s ease forwards;
    opacity: 0;
  }

  h2 {
    font-weight: 400;
    font-size: 1.3rem;
    margin-bottom: 2em;
    opacity: 0.85;
  }

  /* Animate heading from top */
  @keyframes slideDown {
    to {
      opacity: 1;
      transform: translateY(0);
    }
    from {
      opacity: 0;
      transform: translateY(-30px);
    }
  }

  /* Animated underline */
  h1 span {
    position: relative;
    display: inline-block;
    color: #fff;
  }
  h1 span::after {
    content: '';
    position: absolute;
    left: 0;
    bottom: -10px;
    width: 100%;
    height: 4px;
    background: #ff6600;
    border-radius: 3px;
    transform-origin: left center;
    animation: underlineGrow 2s ease forwards;
  }

  @keyframes underlineGrow {
    from {
      transform: scaleX(0);
      opacity: 0;
    }
    to {
      transform: scaleX(1);
      opacity: 1;
    }
  }

  /* Live demo section */
  .live-demo {
    margin-top: 30px;
    opacity: 0;
    animation: fadeIn 2s ease 1.5s forwards;
  }
  .live-demo a {
    text-decoration: none;
    color: #ff0000;
    background: #fff;
    padding: 12px 32px;
    border-radius: 50px;
    font-weight: 700;
    font-size: 1.1rem;
    box-shadow: 0 8px 15px rgba(255, 69, 0, 0.4);
    transition: all 0.3s ease;
    display: inline-block;
  }
  .live-demo a:hover {
    background: #ff3300;
    color: white;
    box-shadow: 0 15px 20px rgba(255, 33, 0, 0.7);
    transform: translateY(-4px);
  }

  /* Fade in animation */
  @keyframes fadeIn {
    to {
      opacity: 1;
    }
    from {
      opacity: 0;
    }
  }

  /* Footer Branding */
  footer {
    position: fixed;
    bottom: 15px;
    font-size: 0.9rem;
    color: #eee;
    letter-spacing: 0.05em;
    user-select: none;
    font-weight: 300;
  }

  /* Animated subtle pulse background effect */
  .pulse-bg {
    position: fixed;
    top: 50%;
    left: 50%;
    width: 400px;
    height: 400px;
    background: radial-gradient(circle, rgba(255,69,0,0.25) 0%, transparent 70%);
    border-radius: 50%;
    animation: pulse 4s ease-in-out infinite;
    transform: translate(-50%, -50%);
    z-index: 0;
  }

  @keyframes pulse {
    0% {
      transform: translate(-50%, -50%) scale(1);
      opacity: 0.6;
    }
    50% {
      transform: translate(-50%, -50%) scale(1.15);
      opacity: 0.3;
    }
    100% {
      transform: translate(-50%, -50%) scale(1);
      opacity: 0.6;
    }
  }
</style>
</head>
<body>
  <div class="pulse-bg"></div>
  <div class="container" role="main" aria-label="Project Introduction">
    <h1><span>Project 2</span></h1>
    <h2>of our learning community <strong>"Coders and Programmers"</strong></h2>
    <p>Welcome to the exciting journey of coding and programming! This project showcases skills we are building together.</p>

    <div class="live-demo">
      <a href="https://example.com/live-demo" target="_blank" rel="noopener noreferrer" aria-label="Live Demo Link">Live Demo</a>
    </div>
  </div>

  <footer>© 2024 Coders and Programmers Community</footer>

  <script>
    // Animate header fade in with delay for underline after page load
    document.addEventListener('DOMContentLoaded', () => {
      const heading = document.querySelector('h1');
      heading.style.opacity = '1';
      heading.style.transform = 'translateY(0)';
    });
  </script>
</body>
</html>


