# mini-air-cooler-<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mini Air Cooler</title>

<style>
body {
  margin: 0;
  font-family: Arial;
  background: #0f172a;
  color: white;
  text-align: center;
}

.container { padding: 20px; }

img {
  width: 90%;
  max-width: 300px;
  border-radius: 10px;
}

.btn {
  background: #ef4444;
  padding: 12px 25px;
  border: none;
  color: white;
  font-size: 18px;
  border-radius: 5px;
  cursor: pointer;
}

.box {
  background: #1e293b;
  margin: 10px;
  padding: 15px;
  border-radius: 10px;
}

.review {
  background: #020617;
  margin: 10px;
  padding: 15px;
  border-radius: 10px;
}

.timer {
  font-size: 24px;
  color: #facc15;
  margin: 15px 0;
}

input, textarea {
  width: 90%;
  padding: 10px;
  margin: 8px;
  border-radius: 5px;
  border: none;
}
</style>
</head>

<body>

<div class="container">

  <!-- Product Image -->
  <img src="YOUR_IMAGE_LINK_HERE" alt="Mini Cooler">

  <!-- Hero -->
  <h1>Stay Cool Anywhere ❄️</h1>
  <p>Mini Air Cooler with Mist & LED Light</p>
  <button class="btn">Buy Now</button>

  <!-- Timer -->
  <div class="timer" id="timer">⏳ Offer Ends In: 10:00</div>

  <!-- Features -->
  <div class="box">5 Nozzle Mist Cooling</div>
  <div class="box">Ice Cooling System</div>
  <div class="box">USB Powered</div>
  <div class="box">Silent Fan</div>

  <!-- Reviews -->
  <h2>⭐ Customer Reviews</h2>
  <div class="review">“খুব ঠান্ডা বাতাস দেয়! 😍”</div>
  <div class="review">“Small but powerful 💯”</div>
  <div class="review">“Worth every taka 🔥”</div>

  <!-- Order -->
  <h2>🛒 Order Now</h2>

  <input type="text" id="name" placeholder="Your Name">
  <input type="tel" id="phone" placeholder="Phone Number">
  <textarea id="address" placeholder="Address"></textarea>

  <button class="btn" onclick="order()">Confirm Order</button>

</div>

<script>
// Countdown Timer
var time = 600;
setInterval(function(){
  var min = Math.floor(time/60);
  var sec = time % 60;
  document.getElementById("timer").innerHTML =
  "⏳ Offer Ends In: " + min + ":" + (sec<10?"0"+sec:sec);
  time--;
},1000);

// WhatsApp Order
function order(){
  var name = document.getElementById("name").value;
  var phone = document.getElementById("phone").value;
  var address = document.getElementById("address").value;

  if(name=="" || phone=="" || address==""){
    alert("Fill all fields!");
    return;
  }

  var msg = "Order:%0AName: "+name+"%0APhone: "+phone+"%0AAddress: "+address;

  window.open("https://wa.me/880XXXXXXXXXX?text="+msg);
}
</script>

</body>
</html>
