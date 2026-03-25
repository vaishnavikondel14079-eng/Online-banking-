# Online-banking-
Online banking system 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bank Demo Login</title>

<style>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  background: #eef2f7;
}

.container {
  max-width: 350px;
  margin: 80px auto;
  background: white;
  padding: 25px;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

h2 {
  text-align: center;
}

input {
  width: 100%;
  padding: 12px;
  margin-top: 10px;
  border-radius: 8px;
  border: 1px solid #ccc;
}

button {
  width: 100%;
  padding: 12px;
  margin-top: 15px;
  border: none;
  border-radius: 8px;
  background: #1e90ff;
  color: white;
  font-size: 16px;
  cursor: pointer;
}

button:hover {
  background: #0c7cd5;
}

.hidden {
  display: none;
}

.dashboard {
  text-align: center;
}
</style>
</head>

<body>

<!-- LOGIN -->
<div class="container" id="loginBox">
  <h2>🏦 Bank Login</h2>
  <input type="text" placeholder="User ID" id="user">
  <input type="password" placeholder="Password" id="pass">
  <button onclick="login()">Login</button>
</div>

<!-- OTP -->
<div class="container hidden" id="otpBox">
  <h2>🔐 Enter OTP</h2>
  <p style="text-align:center;">Demo OTP: <b>1234</b></p>
  <input type="text" placeholder="Enter OTP" id="otp">
  <button onclick="verifyOTP()">Verify OTP</button>
</div>

<!-- DASHBOARD -->
<div class="container hidden dashboard" id="dashboard">
  <h2>Welcome!</h2>
  <p>Account Holder: Vaishnavi</p>
  <h3 style="color:green;">Balance: ₹25,000</h3>
  <button onclick="alert('Demo Transfer Successful')">Transfer Money</button>
</div>

<script>
function login() {
  let user = document.getElementById("user").value;
  let pass = document.getElementById("pass").value;

  if(user && pass) {
    document.getElementById("loginBox").classList.add("hidden");
    document.getElementById("otpBox").classList.remove("hidden");
  } else {
    alert("Enter valid details");
  }
}

function verifyOTP() {
  let otp = document.getElementById("otp").value;

  if(otp === "1234") {
    document.getElementById("otpBox").classList.add("hidden");
    document.getElementById("dashboard").classList.remove("hidden");
  } else {
    alert("Invalid OTP");
  }
}
</script>

</body>
</html>
