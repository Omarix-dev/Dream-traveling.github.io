<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Download Baseball 9 - Free Mobile Game</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary: #16a34a;
      --primary-dark: #15803d;
      --accent: #facc15;
      --light: #f0fdf4;
      --dark: #1f2937;
      --gray: #6b7280;
    }

    body {
      font-family: 'Poppins', sans-serif;
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #e0f2f1 0%, #f8fafc 100%);
      color: var(--dark);
    }

    .container {
      max-width: 1000px;
      margin: 0 auto;
      padding: 2rem;
    }

    .hero {
      background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
      color: white;
      padding: 4rem 2rem;
      border-radius: 16px;
      text-align: center;
      box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
      position: relative;
      overflow: hidden;
    }

    .hero::before, .hero::after {
      content: "";
      position: absolute;
      border-radius: 50%;
      background: rgba(255, 255, 255, 0.1);
    }

    .hero::before {
      top: -60px;
      right: -60px;
      width: 200px;
      height: 200px;
    }

    .hero::after {
      bottom: -80px;
      left: -80px;
      width: 250px;
      height: 250px;
    }

    .hero h1 {
      font-size: 2.6rem;
      margin-bottom: 1rem;
      font-weight: 700;
    }

    .hero p {
      font-size: 1.2rem;
      margin-bottom: 2rem;
      opacity: 0.9;
    }

    .cta-button {
      background: linear-gradient(to right, var(--accent), #eab308);
      color: #000;
      font-weight: 600;
      border: none;
      padding: 1rem 2.5rem;
      font-size: 1.1rem;
      border-radius: 50px;
      cursor: pointer;
      text-decoration: none;
