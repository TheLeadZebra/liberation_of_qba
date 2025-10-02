---
{"dg-publish":true,"permalink":"/home-page/home-page/","tags":["gardenEntry"]}
---

# Home Page

Welcome to the Wikisite for The Crown of Thorn, a D&D campaign.
```
<!-- 
  To use this in Obsidian, simply copy and paste this entire code block 
  into a note. When you switch to "Reading View", the countdown will appear and start running.
-->
<style>
  /* --- Styling for the countdown container --- */
  .countdown-container {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
    text-align: center;
    background-color: #1a1a1a; /* Dark background for contrast */
    padding: 30px 20px;
    border-radius: 12px;
    border: 1px solid #333;
    max-width: 500px;
    margin: 20px auto;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
  }

  /* --- Styling for the main title --- */
  .countdown-title {
    font-size: 1.5rem;
    font-weight: 600;
    color: #e0e0e0;
    margin-bottom: 25px;
  }

  /* --- Flex container for the timer blocks --- */
  .timer-wrapper {
    display: flex;
    justify-content: center;
    gap: 15px; /* Space between the blocks */
  }

  /* --- Styling for each individual time block (Days, Hours, etc.) --- */
  .time-block {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-color: #2c2c2c;
    border-radius: 8px;
    padding: 15px;
    min-width: 80px;
  }

  /* --- Styling for the large number (e.g., "30") --- */
  .time-value {
    font-size: 2.5rem;
    font-weight: 700;
    color: #ffffff;
    line-height: 1;
  }

  /* --- Styling for the label (e.g., "Days") --- */
  .time-label {
    font-size: 0.8rem;
    text-transform: uppercase;
    color: #999999;
    margin-top: 8px;
  }

  /* --- Styling for the finished message --- */
  .finished-message {
    font-size: 1.8rem;
    font-weight: 600;
    color: #4ade80; /* A nice green color */
  }
</style>

<div id="countdown" class="countdown-container">
  <div class="countdown-title">Countdown to Event</div>
  <div id="timer" class="timer-wrapper">
    <!-- Days -->
    <div class="time-block">
      <div id="days" class="time-value">0</div>
      <div class="time-label">Days</div>
    </div>
    <!-- Hours -->
    <div class="time-block">
      <div id="hours" class="time-value">0</div>
      <div class="time-label">Hours</div>
    </div>
    <!-- Minutes -->
    <div class="time-block">
      <div id="minutes" class="time-value">0</div>
      <div class="time-label">Minutes</div>
    </div>
    <!-- Seconds -->
    <div class="time-block">
      <div id="seconds" class="time-value">0</div>
      <div class="time-label">Seconds</div>
    </div>
  </div>
</div>

<script>
  // --- CONFIGURATION ---
  // Set your target date and time here.
  // IMPORTANT: '2025-10-30T17:00:00Z' represents October 30th, 2025 at 5:00 PM in UTC/GMT.
  // During October, UK time is GMT, so this is the correct setting.
  const targetDate = new Date('2025-10-30T17:00:00Z').getTime();

  // --- COUNTDOWN LOGIC ---
  const countdownFunction = setInterval(() => {
    // Get the current time
    const now = new Date().getTime();

    // Calculate the difference between the target and current time
    const difference = targetDate - now;

    // Check if the countdown has finished
    if (difference < 0) {
      clearInterval(countdownFunction);
      const timerElement = document.getElementById('timer');
      timerElement.innerHTML = `<div class="finished-message">Countdown Finished!</div>`;
      return;
    }

    // Calculate time units
    const days = Math.floor(difference / (1000 * 60 * 60 * 24));
    const hours = Math.floor((difference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    const minutes = Math.floor((difference % (1000 * 60 * 60)) / (1000 * 60));
    const seconds = Math.floor((difference % (1000 * 60)) / 1000);

    // Function to add a leading zero if the number is less than 10
    const formatTime = (time) => (time < 10 ? `0${time}` : time);

    // Update the HTML elements with the new values
    document.getElementById('days').innerText = formatTime(days);
    document.getElementById('hours').innerText = formatTime(hours);
    document.getElementById('minutes').innerText = formatTime(minutes);
    document.getElementById('seconds').innerText = formatTime(seconds);

  }, 1000); // Run this function every second (1000 milliseconds)
</script>


```
The idea of this site is not so that you will know everything that is coming up, but so that you may know the sort of things your character may know. Use the information here for building a character background, but there's no need to memorise everything, or even anything if that's your preference.

**Character Backstories**: I'm happy to give as much free reign as reasonable here as long as it fits the world. My one main caveat is that you must be wanting to dethrone the tyranical ruler of the island, [[Story/People/Enemies/King Francis Roberts\|King Francis Roberts]], how or why is completely up to you. Further information and more detail will be given during "session Zero's". 

If you feel like it, start here: [[The World/The Island of Qba/History of the Island/History of the Island\|History of the Island]]
To learn about the region in which this campaign will take part, ***[[The World/The Island of Qba/The Island of Qba\|Click Here]]***

Otherwise, the menu is on the left.

There are a lot of work in progress articles, if you would like to know more about a particular topic, let me know.
>[!warning] ***Obligatory statement that everything is fluid until it hits the table***
















---
