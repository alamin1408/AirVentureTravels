<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>AirVenture Travels</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100 font-sans">

  <!-- Header -->
  <header class="bg-blue-700 text-white shadow-md">
    <div class="container mx-auto flex justify-between items-center p-4">
      <h1 class="text-2xl font-bold">AirVenture Travels</h1>
      <nav>
        <ul class="flex space-x-6">
          <li><a href="#home" class="hover:text-gray-300">Home</a></li>
          <li><a href="#packages" class="hover:text-gray-300">Packages</a></li>
          <li><a href="#flights" class="hover:text-gray-300">Flights</a></li>
          <li><a href="#contact" class="hover:text-gray-300">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- Hero -->
  <section id="home" class="bg-blue-100 py-20 text-center">
    <div class="container mx-auto px-4">
      <h2 class="text-4xl md:text-5xl font-bold mb-4">Welcome to AirVenture Travels</h2>
      <p class="text-gray-700 mb-6">Your trusted partner for flight booking, travel packages, and unforgettable journeys.</p>
      <a href="#packages" class="bg-blue-700 text-white px-6 py-3 rounded hover:bg-blue-800 transition">Explore Packages</a>
    </div>
  </section>

  <!-- Packages -->
  <section id="packages" class="py-20 bg-gray-50">
    <div class="container mx-auto px-4 text-center">
      <h2 class="text-3xl md:text-4xl font-bold mb-12">Travel Packages</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8">
        <div class="bg-white shadow-lg rounded-xl p-6 hover:scale-105 transform transition duration-300">
          <img src="assets/dubai.jpg" alt="Dubai Adventure" class="rounded mb-4 w-full h-48 object-cover">
          <h3 class="text-xl md:text-2xl font-semibold mb-3">Dubai Adventure</h3>
          <p class="text-gray-700 mb-4">5 Nights / 6 Days, Flights + Hotel included</p>
          <span class="font-bold text-blue-700 text-lg">৳65,000</span>
        </div>

        <div class="bg-white shadow-lg rounded-xl p-6 hover:scale-105 transform transition duration-300">
          <img src="assets/thailand.jpg" alt="Thailand Getaway" class="rounded mb-4 w-full h-48 object-cover">
          <h3 class="text-xl md:text-2xl font-semibold mb-3">Thailand Getaway</h3>
          <p class="text-gray-700 mb-4">4 Nights / 5 Days, Flights + Hotel included</p>
          <span class="font-bold text-blue-700 text-lg">৳55,000</span>
        </div>

        <div class="bg-white shadow-lg rounded-xl p-6 hover:scale-105 transform transition duration-300">
          <img src="assets/europe.jpg" alt="Europe Explorer" class="rounded mb-4 w-full h-48 object-cover">
          <h3 class="text-xl md:text-2xl font-semibold mb-3">Europe Explorer</h3>
          <p class="text-gray-700 mb-4">7 Nights / 8 Days, Flights + Hotel included</p>
          <span class="font-bold text-blue-700 text-lg">৳150,000</span>
        </div>
      </div>
    </div>
  </section>

  <!-- Flights -->
  <section id="flights" class="bg-gray-200 py-20">
    <div class="container mx-auto text-center px-4">
      <h2 class="text-3xl md:text-4xl font-bold mb-10">Book Your Flight</h2>
      <form class="max-w-xl mx-auto bg-white shadow-md rounded p-6 space-y-4" onsubmit="return false;">
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
          <div>
            <label class="block text-left mb-1">From</label>
            <input type="text" class="w-full border border-gray-300 rounded px-3 py-2" placeholder="City or Airport">
          </div>
          <div>
            <label class="block text-left mb-1">To</label>
            <input type="text" class="w-full border border-gray-300 rounded px-3 py-2" placeholder="City or Airport">
          </div>
        </div>
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
          <div>
            <label class="block text-left mb-1">Departure Date</label>
            <input type="date" class="w-full border border-gray-300 rounded px-3 py-2">
          </div>
          <div>
            <label class="block text-left mb-1">Return Date</label>
            <input type="date" class="w-full border border-gray-300 rounded px-3 py-2">
          </div>
        </div>
        <button type="submit" class="w-full bg-blue-700 text-white py-2 rounded hover:bg-blue-800 transition">Search Flights</button>
      </form>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="py-20">
    <div class="container mx-auto text-center px-4">
      <h2 class="text-3xl md:text-4xl font-bold mb-10">Contact Us</h2>

      <!-- ********** IMPORTANT: replace the action URL with your Google Apps Script / Formspree URL ********** -->
      <form id="contactForm" action="CONTACT_FORM_ACTION_URL" method="POST"
            class="max-w-lg mx-auto bg-white shadow-md rounded p-6 space-y-4">
        <input type="text" name="name" placeholder="Your Name" required class="w-full border border-gray-300 rounded px-3 py-2">
        <input type="email" name="email" placeholder="Your Email" required class="w-full border border-gray-300 rounded px-3 py-2">
        <textarea name="message" placeholder="Message" required class="w-full border border-gray-300 rounded px-3 py-2"></textarea>

        <!-- optional: disable server-side captcha -->
        <input type="hidden" name="_captcha" value="false">

        <button type="submit" class="w-full bg-blue-700 text-white py-2 rounded hover:bg-blue-800 transition">Send Message</button>
      </form>

      <!-- success popup -->
      <div id="successPopup" class="hidden fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50">
        <div class="bg-white rounded-lg shadow-lg p-6 max-w-sm text-center">
          <h3 class="text-xl font-semibold mb-3 text-green-600">✅ Message Sent!</h3>
          <p class="text-gray-600 mb-4">Thank you — we will reply soon.</p>
          <button onclick="closePopup()" class="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700 transition">OK</button>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-blue-700 text-white py-6 mt-10">
    <div class="container mx-auto text-center px-4">
      <div class="flex flex-col md:flex-row justify-between items-center">
        <span>&copy; 2025 AirVenture Travels. All rights reserved.</span>
        <div class="mt-3 md:mt-0 flex space-x-4">
          <a href="#" class="hover:text-gray-300">Facebook</a>
          <a href="#" class="hover:text-gray-300">Instagram</a>
          <a href="#" class="hover:text-gray-300">Twitter</a>
        </div>
      </div>
    </div>
  </footer>

<script>
  // contact form submit handler (works with Google Apps Script or Formspree URL)
  const form = document.getElementById('contactForm');
  const popup = document.getElementById('successPopup');

  form.addEventListener('submit', async function(e) {
    e.preventDefault();

    // ensure action url replaced
    if (!form.action || form.action === 'CONTACT_FORM_ACTION_URL') {
      alert('দয়া করে CONTACT_FORM_ACTION_URL আপনার Google Apps Script (or form) URL দিয়ে প্রতিস্থাপন করুন।');
      return;
    }

    try {
      const res = await fetch(form.action, {
        method: 'POST',
        body: new FormData(form),
        headers: { Accept: 'application/json' }
      });

      if (res.ok) {
        form.reset();
        popup.classList.remove('hidden');
      } else {
        // some endpoints (Google Apps Script) return text; treat 200 as ok
        const text = await res.text();
        if (res.status === 200 || text.toLowerCase().includes('success')) {
          form.reset();
          popup.classList.remove('hidden');
        } else {
          throw new Error('submission failed');
        }
      }
    } catch (err) {
      console.error(err);
      alert('❌ Something went wrong while sending. Check your action URL and console.');
    }
  });

  function closePopup() {
    document.getElementById('successPopup').classList.add('hidden');
  }
</script>

</body>
</html>
