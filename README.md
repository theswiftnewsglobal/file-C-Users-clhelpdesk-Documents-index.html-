<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Swift News</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background: #f4f6f8;
      color: #333;
    }

    header {
      background: #111827;
      color: white;
      padding: 20px;
      text-align: center;
    }

    header h1 {
      margin: 0;
      font-size: 28px;
    }

    nav {
      background: #1f2937;
      padding: 10px;
      text-align: center;
    }

    nav a {
      color: white;
      margin: 0 15px;
      text-decoration: none;
      font-weight: bold;
    }

    .container {
      max-width: 1000px;
      margin: 20px auto;
      padding: 0 15px;
    }

    .controls {
      text-align: center;
      margin-bottom: 15px;
    }

    button {
      padding: 10px 15px;
      border: none;
      background: #111827;
      color: white;
      border-radius: 6px;
      cursor: pointer;
    }

    button:hover {
      background: #374151;
    }

    .news-card {
      background: white;
      margin-bottom: 15px;
      padding: 15px;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    .news-card h2 {
      margin-top: 0;
      font-size: 20px;
    }

    .news-card p {
      color: #555;
    }

    footer {
      text-align: center;
      padding: 15px;
      background: #111827;
      color: white;
      margin-top: 20px;
    }
  </style>
</head>
<body>

<header>
  <h1>Swift News</h1>
  <p>Fast, Reliable, Up-to-date News</p>
</header>

<nav>
  <a href="#">Home</a>
  <a href="#">World</a>
  <a href="#">Tech</a>
  <a href="#">Sports</a>
  <a href="#">Contact</a>
</nav>

<div class="container">

  <div class="controls">
    <button onclick="loadNews()">Refresh News</button>
  </div>

  <div id="news"></div>

</div>

<footer>
  <p>&copy; 2026 Swift News. All rights reserved.</p>
</footer>

<script>
const sampleNews = [
  {
    title: "AI Breakthrough Changes Tech Industry",
    desc: "A new AI model is making waves across global tech companies."
  },
  {
    title: "Global Markets Show Positive Growth",
    desc: "Stock markets around the world are trending upward this week."
  },
  {
    title: "Sports Update: Underdog Wins Championship",
    desc: "A surprising victory shocks fans in last night’s final match."
  },
  {
    title: "Space Exploration: New Planet Discovered",
    desc: "Scientists identify a potentially habitable exoplanet."
  }
];

function loadNews() {
  const container = document.getElementById("news");
  container.innerHTML = "";

  sampleNews.forEach(item => {
    const card = document.createElement("div");
    card.className = "news-card";
    card.innerHTML = `
      <h2>${item.title}</h2>
      <p>${item.desc}</p>
    `;
    container.appendChild(card);
  });
}

// Load news on first open
loadNews();
</script>

</body>
</html>

A simple real-time news dashboard with dynamic updates and a clean UI.
