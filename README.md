<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Win a Dream Caribbean Getaway!</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://unpkg.com/@heroicons/vue@1.0.6/outline"></script>
</head>
<body class="bg-gradient-to-br from-blue-100 to-blue-300 text-gray-800">

  <main class="max-w-3xl mx-auto p-6 sm:p-10 bg-white rounded-xl shadow-xl mt-10">
    <header class="text-center">
      <h1 class="text-3xl sm:text-4xl font-bold text-blue-700">🌴 Win a Dream Caribbean Getaway for Two!</h1>
      <p class="mt-3 text-gray-600">All-expenses-paid vacation — enter now!</p>
    </header>

    <div class="mt-6">
      <img src="https://images.unsplash.com/photo-1559128010-7c1ad6e1b6a5?auto=format&fit=crop&w=800&q=80" alt="Caribbean Beach Resort" class="rounded-lg w-full h-64 object-cover shadow-md">
    </div>

    <div class="text-center mt-6 text-lg font-semibold text-orange-600">
      Time remaining to enter: <span id="timer" class="font-bold">--:--:--</span>
    </div>

    <section class="mt-8 bg-blue-50 p-4 rounded-lg border-l-4 border-blue-500">
      <h2 class="text-xl font-bold mb-2">Your Prize Includes:</h2>
      <ul class="list-disc pl-5 space-y-1 text-gray-700">
        <li>7 nights in a 5-star Caribbean resort</li>
        <li>Round-trip airfare for two</li>
        <li>All-inclusive food & drinks</li>
        <li>Private beach access</li>
        <li>Spa credits worth $500</li>
        <li>Total value: $8,500</li>
      </ul>
    </section>

    <section class="mt-8">
      <h2 class="text-2xl font-semibold mb-4 text-center">Enter Now!</h2>
      <form class="space-y-4" id="entry-form">
        <div>
          <label class="block font-medium mb-1" for="email">Email Address</label>
          <input type="email" id="email" required placeholder="example@email.com"
                 class="w-full border-gray-300 rounded px-4 py-2 shadow-sm focus:outline-none focus:ring-2 focus:ring-blue-400"/>
        </div>
        <div>
          <label class="block font-medium mb-1" for="zip">Zip Code (optional)</label>
          <input type="text" id="zip" placeholder="12345"
                 class="w-full border-gray-300 rounded px-4 py-2 shadow-sm"/>
        </div>
        <button type="submit"
                class="w-full bg-orange-500 hover:bg-orange-600 text-white font-bold py-3 rounded transition-all duration-300">
          🎉 Enter to Win Now!
        </button>
      </form>
      <p class="text-xs text-gray-500 mt-4">
        No purchase necessary. Must be 18+. By entering, you agree to receive occasional promotional emails.
      </p>
    </section>

    <footer class="text-center text-sm text-gray-600 mt-10">
      <p><strong>Over 250,000 entries so far — don’t miss your chance!</strong></p>
      <p class="mt-1">Offer ends soon. Enter today!</p>
    </footer>
  </main>

  <script>
    // Countdown timer (24 hours)
    const targetTime = new Date().getTime() + 24 * 60 * 60 * 1000;
    const timerEl = document.getElementById('timer');

    function updateTimer() {
      const now = new Date().getTime();
      const diff = targetTime - now;

      if (diff <= 0) {
        timerEl.textContent = "00:00:00";
        return;
      }

      const hours = String(Math.floor((diff / (1000 * 60 * 60)) % 24)).padStart(2, '0');
      const minutes = String(Math.floor((diff / (1000 * 60)) % 60)).padStart(2, '0');
      const seconds = String(Math.floor((diff / 1000) % 60)).padStart(2, '0');

      timerEl.textContent = `${hours}:${minutes}:${seconds}`;
    }

    setInterval(updateTimer, 1000);
    updateTimer();

    // Form handler
    document.getElementById("entry-form").addEventListener("submit", function(e) {
      e.preventDefault();
      alert("✅ Entry received! Good luck!");
    });
  </script>
</body>
</html>
