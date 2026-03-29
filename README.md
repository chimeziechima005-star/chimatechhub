# chimatechhub
Welcome to Chimatechhub!
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ChimaTech Hub</title>

<script src="https://js.paystack.co/v1/inline.js"></script>

<style>
body {
  margin:0;
  font-family: 'Segoe UI', sans-serif;
  background: radial-gradient(circle at top, #0a0f2c, #020617);
  color:white;
  text-align:center;
}

header {
  padding:60px 20px;
}

h1 {
  font-size:3rem;
  background: linear-gradient(90deg,#00f0ff,#007bff);
  -webkit-background-clip:text;
  color:transparent;
}

.tag {
  opacity:0.7;
}

.container {
  padding:20px;
}

.card {
  background: rgba(255,255,255,0.05);
  backdrop-filter: blur(10px);
  border:1px solid rgba(255,255,255,0.1);
  margin:20px auto;
  padding:20px;
  border-radius:15px;
  max-width:400px;
  box-shadow:0 0 20px rgba(0,0,255,0.2);
}

.price {
  font-size:1.5rem;
  color:#00ffcc;
  margin:10px 0;
}

button {
  padding:12px 20px;
  border:none;
  border-radius:10px;
  background:#00c853;
  color:white;
  font-weight:bold;
  cursor:pointer;
}

button:hover {
  background:#00e676;
}

.whatsapp {
  margin-top:20px;
  display:inline-block;
  padding:15px 25px;
  background:#25D366;
  border-radius:10px;
  color:white;
  text-decoration:none;
  font-weight:bold;
}

footer {
  margin-top:40px;
  padding:20px;
  opacity:0.6;
}
</style>
</head>

<body>

<header>
  <h1>👑 ChimaTech Hub</h1>
  <p class="tag">Boost your social media to the next level 🚀</p>
</header>

<div class="container">

  <div class="card">
    <h2>📈 Instagram Boost</h2>
    <p>Followers + Likes</p>
    <div class="price">₦5,000</div>
    <button onclick="payNow(5000)">Pay Now</button>
  </div>

  <div class="card">
    <h2>🎵 TikTok Boost</h2>
    <p>Followers + Views</p>
    <div class="price">₦5,000</div>
    <button onclick="payNow(5000)">Pay Now</button>
  </div>

  <div class="card">
    <h2>🌍 Foreign Numbers</h2>
    <p>USA 🇺🇸 & UK 🇬🇧</p>
    <div class="price">₦3,000</div>
    <button onclick="payNow(3000)">Pay Now</button>
  </div>

  <a class="whatsapp" href="https://wa.me/2347049335958">
    💬 Chat on WhatsApp
  </a>

</div>

<footer>
© 2026 ChimaTech Hub | Secure Payments 🔒
</footer>

<script>
function payNow(amount) {
  var handler = PaystackPop.setup({
    key: 'YOUR_PUBLIC_KEY_HERE', // replace this
    email: 'customer@email.com',
    amount: amount * 100,
    currency: "NGN",
    callback: function(response){
      alert('Payment successful! Ref: ' + response.reference);
    },
    onClose: function(){
      alert('Transaction cancelled');
    }
  });
  handler.openIframe();
}
</script>

</body>
</html>
