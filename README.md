# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨




<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Responsive Layout</title>
<style>
  body, ul {
    margin: 0; padding: 0; box-sizing: border-box;
    font-family: Arial, sans-serif;
  }
  nav {
    display: flex; justify-content: space-between; align-items: center;
    background: #004466; padding: 1rem 2rem; color: white;
  }
  nav .logo {
    font-weight: bold; font-size: 1.3rem;
  }
  nav ul {
    display: flex; gap: 1.5rem; list-style: none;
  }
  nav a {
    color: white; text-decoration: none; font-weight: 500;
  }
  nav a:hover {
    color: #ffcc00;
  }
  .container {
    display: grid;
    grid-template-columns: 250px 1fr;
    grid-template-areas:
      "sidebar header"
      "sidebar main"
      "sidebar footer";
    min-height: 100vh;
  }
  header {
    grid-area: header; background: #f0f4f8; padding: 1rem 2rem;
    font-weight: 600; border-bottom: 1px solid #ccc;
  }
  aside {
    grid-area: sidebar; background: #e0e7f3; padding: 1rem;
  }
  main {
    grid-area: main; padding: 1rem 2rem; background: #fff;
  }
  footer {
    grid-area: footer; background: #004466; color: white;
    text-align: center; padding: 1rem 2rem; font-size: 0.9rem;
  }

  /* Tablet */
  @media (max-width: 900px) {
    .container {
      grid-template-columns: 1fr;
      grid-template-areas:
        "header"
        "main"
        "sidebar"
        "footer";
    }
  }
  /* Mobile */
  @media (max-width: 600px) {
    nav {
      flex-direction: column; align-items: flex-start; gap: 0.5rem;
    }
    nav ul {
      flex-direction: column; gap: 0.5rem; width: 100%;
    }
    nav a {
      display: block; width: 100%;
    }
    main, header, aside, footer {
      padding: 1rem;
    }
  }
</style>
</head>
<body>

<nav>
  <div class="logo">Brand</div>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">Features</a></li>
    <li><a href="#">Pricing</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>

<div class="container">
  <header>Welcome!</header>
  <aside>
    <h3>Sidebar</h3>
    <ul>
      <li><a href="#">Dashboard</a></li>
      <li><a href="#">Profile</a></li>
      <li><a href="#">Settings</a></li>
    </ul>
  </aside>
  <main>
    <h2>Main Content</h2>
    <p>This layout adapts across devices using CSS Grid and Flexbox.</p>
  </main>
  <footer>&copy; 2025 Brand</footer>
</div>

</body>
</html>
