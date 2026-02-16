# Isma1982.github.io
index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Ismail Muhammad - IT Security</title>
  <style>
    body { font-family: Arial, sans-serif; max-width: 800px; margin: 40px auto; padding: 20px; line-height: 1.6; background: #fff; color: #333; }
    h1 { color: #2c3e50; }
    .contact { background: #f8f9fa; padding: 15px; border-radius: 5px; margin: 20px 0; }
    footer { margin-top: 30px; color: #7f8c8d; font-size: 0.9em; }
    a { color: #3498db; text-decoration: none; }
    a:hover { text-decoration: underline; }
  </style>
</head>
<body>
  <h1>Ismail Muhammad</h1>
  <p><strong>IT Security Professional</strong></p>
  
  <div class="contact">
    📍 Tripoli, Libya | From Maiduguri, Nigeria<br>
    ✉️ <a href="mailto:ismailzola33@gmail.com">ismailzola33@gmail.com</a><br>
    📞 +218 91 102 5231
  </div>

  <h2>About Me</h2>
  <p>Certified in <strong>IT Security by Google Career Certificates</strong>. I specialize in networking fundamentals, Linux systems, and cybersecurity best practices. I’m building real-world skills to contribute to secure digital environments—while preparing for opportunities in Europe.</p>

  <h2>Skills</h2>
  <ul>
    <li>Network Security & Best Practices</li>
    <li>Linux Command Line</li>
    <li>Basic Python & JavaScript</li>
    <li>Technical Documentation</li>
    <li>Problem Solving Under Constraints</li>
  </ul>

  <h2>Languages</h2>
  <p>English (Fluent) | Hausa (Native) | Arabic (Conversational) | Spanish (Learning)</p>

  <footer>
    Built with HTML & CSS | Hosted on GitHub Pages
  </footer>
</body>
</html> <!-- Password Strength Checker -->
<h2>Password Strength Checker</h2>
<p>Test if your password meets basic security standards:</p>
<input type="password" id="passwordInput" placeholder="Type a password..." style="width: 100%; padding: 10px; margin: 10px 0; border: 1px solid #ccc; border-radius: 4px;">
<div id="result" style="margin-top: 10px; padding: 10px; border-radius: 4px;"></div>

<script>
function checkPasswordStrength(password) {
  let messages = [];
  let isValid = true;

  // Rule 1: At least 8 characters
  if (password.length < 8) {
    messages.push("❌ Too short – use at least 8 characters.");
    isValid = false;
  }

  // Rule 2: Contains a number
  if (!/\d/.test(password)) {
    messages.push("⚠️ Add at least one number (0-9).");
    isValid = false;
  }

  // Rule 3: Contains a special character
  if (!/[!@#$%^&*(),.?":{}|<>]/.test(password)) {
    messages.push("⚠️ Add a symbol (e.g., !, @, #, $).");
    isValid = false;
  }

  // Rule 4: Contains uppercase letter
  if (!/[A-Z]/.test(password)) {
    messages.push("⚠️ Add an uppercase letter (A-Z).");
    isValid = false;
  }

  if (isValid) {
    return "✅ Strong password! Good job.";
  } else {
    return messages.join("<br>");
  }
}

// Real-time checking
document.getElementById("passwordInput").addEventListener("input", function() {
  const password = this.value;
  const resultDiv = document.getElementById("result");
  
  if (password === "") {
    resultDiv.innerHTML = "";
    resultDiv.style.backgroundColor = "";
  } else {
    const feedback = checkPasswordStrength(password);
    resultDiv.innerHTML = feedback;
    resultDiv.style.backgroundColor = feedback.includes("✅") ? "#d4edda" : "#f8d7da";
  }
});
</script>
