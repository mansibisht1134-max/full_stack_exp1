<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Admin Dashboard</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <style>
    :root {
      --bg: #f0f0f0;
      --text: #333;
      --card: #ffffff;
    }

    [data-theme="dark"] {
      --bg: #1a1a1a;
      --text: #f9f9f9;
      --card: #2b2b2b;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: var(--bg);
      color: var(--text);
      transition: background 0.3s, color 0.3s;
    }

    header {
      background-color: var(--card);
      padding: 1rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    header h1 {
      margin: 0;
      font-size: 1.5rem;
    }

    button {
      padding: 8px 16px;
      font-size: 1rem;
      background-color: #007bff;
      color: #fff;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }

    main {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1rem;
      padding: 2rem;
    }

    .card {
      background-color: var(--card);
      padding: 1.5rem;
      border-radius: 10px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.05);
    }

    .card h2 {
      margin-top: 0;
      font-size: 1.2rem;
    }

    @media (max-width: 600px) {
      header {
        flex-direction: column;
        align-items: flex-start;
        gap: 0.5rem;
      }
    }
  </style>
</head>
<body data-theme="light">
  <header>
    <h1>Admin Dashboard</h1>
    <button onclick="toggleTheme()">Toggle Theme</button>
  </header>

  <main>
    <div class="card">
      <h2>User Stats</h2>
      <p>Users Online: 153</p>
    </div>
    <div class="card">
      <h2>Sales</h2>
      <p>Revenue Today: ₹8,200</p>
    </div>
    <div class="card">
      <h2>Reports</h2>
      <p>3 new reports generated</p>
    </div>
    <div class="card">
      <h2>Notifications</h2>
      <p>7 unread messages</p>
    </div>
  </main>

  <script>
    function toggleTheme() {
      const current = document.body.getAttribute("data-theme");
      document.body.setAttribute("data-theme", current === "dark" ? "light" : "dark");
    }
  </script>
</body>
</html>

