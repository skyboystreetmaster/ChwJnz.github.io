# 🌐 Welcome 🌐

---

![Hero Image]([https://cdn.7tv.app/emote/01GYHZ0RT8000FQ4GSSD7H5Y4N/3x.webp "Welcome to Our World")

<button id="theme-toggle">🌙 Toggle Dark Mode</button>
---


<style>
  /* Default Light Mode */
  body {
      background-color: #ffffff;
      color: #333333;
      font-family: Arial, sans-serif;
  }

  /* Dark Mode */
  body.dark-mode {
      background-color: #1e1e1e;
      color: #f5f5f5;
  }

  /* Styling for the toggle button */
  #theme-toggle {
      padding: 10px;
      cursor: pointer;
      background-color: #333333;
      color: #ffffff;
      border: none;
      border-radius: 5px;
      position: fixed;
      top: 20px;
      right: 20px;
  }
  body.dark-mode #theme-toggle {
      background-color: #f5f5f5;
      color: #333333;
  }
</style>

<script>
  // JavaScript for theme toggle
  document.addEventListener("DOMContentLoaded", function() {
      const themeToggle = document.getElementById("theme-toggle");
      if (localStorage.getItem("theme") === "dark") {
          document.body.classList.add("dark-mode");
      }

      themeToggle.addEventListener("click", () => {
          document.body.classList.toggle("dark-mode");

          if (document.body.classList.contains("dark-mode")) {
              themeToggle.innerText = "☀️ Toggle Light Mode";
              localStorage.setItem("theme", "dark");
          } else {
              themeToggle.innerText = "🌙 Toggle Dark Mode";
              localStorage.removeItem("theme");
          }
      });
  });
</script>
