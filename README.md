# Swiftgrow-AI
SwiftGrow AI helps small and local businesses grow faster using AI-powered websites, smart chatbots, and WhatsApp automation. We help businesses get more customers, respond instantly to leads, and save time using simple, affordable technology.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>SwiftGrow AI – Grow Your Business Faster</title>
  <meta name="description" content="SwiftGrow AI helps small businesses grow using AI-powered websites, chatbots, and automation." />
  <style>
    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      background: #0f172a;
      color: #e5e7eb;
    }
    header {
      padding: 60px 20px;
      text-align: center;
      background: linear-gradient(135deg, #2563eb, #22c55e);
      color: white;
    }
    header h1 {
      font-size: 3rem;
      margin-bottom: 10px;
    }
    header p {
      font-size: 1.2rem;
      max-width: 600px;
      margin: auto;
    }
    .btn {
      display: inline-block;
      margin-top: 20px;
      padding: 14px 28px;
      background: #0f172a;
      color: white;
      text-decoration: none;
      border-radius: 8px;
      font-weight: bold;
    }
    section {
      padding: 60px 20px;
      max-width: 1100px;
      margin: auto;
    }
    h2 {
      text-align: center;
      font-size: 2.2rem;
      margin-bottom: 40px;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }
    .card {
      background: #020617;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.4);
    }
    .card h3 {
      margin-top: 0;
      color: #22c55e;
    }
    .pricing {
      border: 2px solid #2563eb;
    }
    footer {
      background: #020617;
      padding: 40px 20px;
      text-align: center;
      color: #9ca3af;
    }
  </style>
</head>
<body>

<header>
  <h1>SwiftGrow AI</h1>
  <p>Grow your business faster using AI-powered websites, chatbots, and automation — without tech headaches.</p>
  <a class="btn" href="#contact">Get Free Demo</a>
</header>

<section>
  <h2>What We Do</h2>
  <div class="grid">
    <div class="card">
      <h3>AI Websites</h3>
      <p>Modern, fast websites that convert visitors into customers automatically.</p>
    </div>
    <div class="card">
      <h3>Smart Chatbots</h3>
      <p>24/7 AI chatbots that answer customer questions and capture leads.</p>
    </div>
    <div class="card">
      <h3>Automation</h3>
      <p>Instagram, WhatsApp, and lead automation that saves hours every week.</p>
    </div>
  </div>
</section>

<section>
  <h2>How It Works</h2>
  <div class="grid">
    <div class="card">
      <h3>1. Tell Us About Your Business</h3>
      <p>We understand your goals and audience.</p>
    </div>
    <div class="card">
      <h3>2. We Build & Automate</h3>
      <p>We set up AI tools customized for you.</p>
    </div>
    <div class="card">
      <h3>3. You Get More Customers</h3>
      <p>Relax while AI works for your business.</p>
    </div>
  </div>
</section>

<section>
  <h2>Pricing</h2>
  <div class="grid">
    <div class="card pricing">
      <h3>Starter</h3>
      <p><strong>₹999 / month</strong></p>
      <p>AI Website<br>Basic Chatbot<br>Email Support</p>
      <a class="btn" href="https://rzp.io/l/starter" target="_blank">Pay Now</a>
    </div>
    <div class="card pricing">
      <h3>Growth</h3>
      <p><strong>₹2,999 / month</strong></p>
      <p>Website<br>Chatbot<br>Social Media Automation</p>
      <a class="btn" href="https://rzp.io/l/growth" target="_blank">Pay Now</a>
    </div>
    <div class="card pricing">
      <h3>Pro</h3>
      <p><strong>₹6,999 / month</strong></p>
      <p>Everything Included<br>Lead Automation<br>Priority Support</p>
      <a class="btn" href="https://rzp.io/l/pro" target="_blank">Pay Now</a>
    </div>
  </div>
</section>

<!-- AI Chatbot -->
<div id="chatbot" style="position:fixed;bottom:20px;right:20px;width:300px;background:#020617;border-radius:12px;box-shadow:0 10px 30px rgba(0,0,0,.5);overflow:hidden;">
  <div style="background:#2563eb;color:white;padding:12px;font-weight:bold;">SwiftGrow AI Bot</div>
  <div id="chatArea" style="height:220px;padding:10px;overflow-y:auto;font-size:.9rem;"></div>
  <input id="chatInput" placeholder="Ask me anything..." style="width:100%;padding:10px;border:none;" onkeydown="if(event.key==='Enter')reply()" />
</div>

<script>
  const chatArea = document.getElementById('chatArea');
  function reply() {
    const input = document.getElementById('chatInput');
    const msg = input.value.trim();
    if (!msg) return;
    chatArea.innerHTML += `<div><strong>You:</strong> ${msg}</div>`;

    let bot = "Thanks for your interest! We help businesses grow using AI websites, chatbots, and automation. Click 'Get Free Demo' or WhatsApp us to start.";

    if (msg.toLowerCase().includes('price')) bot = "Our plans start at ₹999/month. Scroll to pricing and click Pay Now.";
    if (msg.toLowerCase().includes('demo')) bot = "Sure! Fill the form and you'll get a WhatsApp demo instantly.";

    setTimeout(() => {
      chatArea.innerHTML += `<div><strong>Bot:</strong> ${bot}</div>`;
      chatArea.scrollTop = chatArea.scrollHeight;
    }, 600);

    input.value = '';
  }
</script>

<section id="contact">
  <h2>Get a Free Demo</h2>
  <div class="card">
    <form onsubmit="sendWhatsApp(event)">
      <input type="text" id="name" placeholder="Your Name" required style="width:100%;padding:12px;margin-bottom:12px;border-radius:6px;border:none;" />
      <input type="email" id="email" placeholder="Your Email" required style="width:100%;padding:12px;margin-bottom:12px;border-radius:6px;border:none;" />
      <input type="text" id="business" placeholder="Your Business" required style="width:100%;padding:12px;margin-bottom:12px;border-radius:6px;border:none;" />
      <button class="btn" type="submit" style="width:100%;">Get Demo on WhatsApp</button>
    </form>
    <p style="text-align:center;margin-top:15px;">or Email us: <strong>hello@swiftgrowai.com</strong></p>
  </div>
</section>

<script>
  function sendWhatsApp(e) {
    e.preventDefault();
    const name = document.getElementById('name').value;
    const email = document.getElementById('email').value;
    const business = document.getElementById('business').value;

    const message = `Hello SwiftGrow AI,%0A%0AName: ${name}%0AEmail: ${email}%0ABusiness: ${business}%0A%0AI want a free demo.`;
    window.open(`https://wa.me/91XXXXXXXXXX?text=${message}`, '_blank');
  }
</script>

<footer>
  <p>© 2025 SwiftGrow AI. All rights reserved.</p>
</footer>

</body>
</html>
