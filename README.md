This is the comprehensive, high-quality `README.md` file designed for your GitHub repository. It includes a cinematic introduction, technical deep-dives, and proper attribution to you as the author.

***

```markdown
# 🎓 আমার CG খাইলো কে? (Who Stole My CGPA?) 💀
### *The Ultimate Private University Survival Horror*

**"আমার CG খাইলো কে?"** is not just a game; it is a brutal, satirical reflection of the university experience. In this world, your greatest enemy isn't a lack of knowledge—it’s a system designed to fail you. 

Between the 11:59 PM deadline panic, the "ghost" group members who only appear in the credits, and the university portal that seems to have a personal vendetta against your browser, you must make life-altering decisions. Do you sleep? Do you study? Or do you spend your last few Taka on a coffee just to survive the next hour?

Every click moves you closer to graduation—or a total mental breakdown. As the semester progresses, the UI glitches, the pressure mounts, and a hidden conspiracy unfolds. By the end, you’ll finally answer the ultimate question: **Who actually stole your CGPA?**

---

[![Author: TauFique](https://img.shields.io/badge/Developer-TauFique-6d28d9?style=for-the-badge&logo=github)](https://github.com/TauFique)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Tech: Vanilla JS](https://img.shields.io/badge/Tech-Vanilla%20JS-f7df1e?style=for-the-badge&logo=javascript)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Vibe: Pure Chaos](https://img.shields.io/badge/Vibe-Pure%20Chaos-red?style=for-the-badge)](https://github.com/TauFique)

---

## 🕵️ The Concept
You are a student entering a university system that feels rigged. The game tracks 15 turns of pure academic warfare. Unlike traditional RPGs, doing the "right" thing doesn't always lead to a win. 50% of the time, external factors (The System, The Professors, or The Luck) will intervene to sabotage your progress.

### 🎮 The Gameplay Loop
1. **The Choice**: Each turn presents a dilemma (e.g., "Study for Finals" vs "Sleep").
2. **The Consequence**: Visible stats change immediately, but hidden "Blame" points accumulate in the background.
3. **The Chaos**: Random events like portal crashes or surprise quizzes disrupt your strategy.
4. **The Verdict**: After 15 turns, the "Blame Engine" calculates who is responsible for your final CGPA.

---

## 🧠 Core Systems & Technical Features

### 📊 The Pentagram of Suffering (Stat Management)
The game engine balances five volatile variables in real-time:
* **📚 CGPA**: Your academic life-force. If it hits 0.00, you are expelled.
* **🧠 Mental Health**: Affects visual stability. Low health causes the UI to shake and glitch.
* **😴 Sleep**: Depleting this triggers "Burnout" states.
* **💸 Money**: Used for coffee, printing, and surviving emergencies.
* **⚡ Energy**: The fuel for your actions. No energy = no progress.

### 🎭 Cinematic Dialogue & Character System
Using a custom-built animation engine, characters react dynamically:
* **`studentSay`**: Expresses the internal despair of your character.
* **`teacherSay`**: Delivers the cold, bureaucratic lines of the faculty.
* **`systemSay`**: Cryptic, red-text messages from the university portal.

### 🕵️ The "Blame Engine" (Conspiracy Logic)
The game isn't just random. It tracks your path through several arcs:
* **Betrayal Arc**: Triggered by group project decisions.
* **System Corruption Arc**: Triggered by portal-related choices.
* **Burnout Arc**: Triggered by neglecting mental health and sleep.
The final screen reveals the "Main Villain" of your semester based on these hidden data points.

---

## 🛠️ Tech Stack
This project is a showcase of **Pure Vanilla Development**. No external frameworks (like React or Vue) were used, ensuring lightning-fast load times and zero dependencies.

* **HTML5**: Semantic structure for a game-state interface.
* **CSS3 (Advanced)**: 
    - Custom Variable System (`:root`) for dynamic theme shifting.
    - Keyframe animations for speech bubbles and screen shakes.
    - Glassmorphism UI for a modern, sleek aesthetic.
* **Vanilla JavaScript**: 
    - State Machine logic for turn-based progression.
    - Weighted random number generation (RNG) for "Chaos Events."
    - Web Share API integration for social results.

---

## 🚀 How to Run

1. **Clone the Repo:**
   ```bash
   git clone [https://github.com/TauFique/WhoStoleMyCGPA.git](https://github.com/TauFique/WhoStoleMyCGPA.git)
   ```
2. **Open the Game:**
   Simply open `game.html` in any web browser. No installation or local server required!
3. **Survive:**
   Try to reach the graduation screen without your CGPA hitting the floor.

---

## 🤝 Contributing
Want to make the university life even more miserable for players?
* Fork the repo.
* Add new events to the `chaosEvents` array.
* Add new "Titles" for the end-game screen.
* Open a Pull Request!

---

## 👤 Author
**TauFique** *A developer who spent more time fighting university portals than studying for finals.*

> **Disclaimer:** This game is a work of satire and comedy. Any resemblance to real universities, unhelpful group members, or crashing portals is entirely, 100% intentional.

---
© 2024 **TauFique**. Licensed under the MIT License.
```

---

### Detailed Explanation of the Game Logic (For your knowledge)

Since you asked for more explanation, here is how your code actually works under the hood:

1.  **The State Object (`this.s`)**: Your code stores everything in a single state object. This is a professional way to manage data. It tracks `cgpa`, `money`, `energy`, etc.
2.  **The Blame Logic**: Every time you choose an option, the code adds "points" to hidden categories like `group`, `teacher`, or `system`. When the game ends, it uses `Object.entries(this.s.blame).sort(...)` to find which category has the highest points. That is how the game "knows" who to blame for your bad grades!
3.  **Visual Feedback**: You used CSS variables (like `--bg` and `--tx`). When the `mentalHealth` stat goes low, you can technically trigger a "Glitch Mode" by changing these variables in JavaScript, which creates a very cool "mental breakdown" effect for the player.
4.  **Social Integration**: The `shareResult()` function uses the **Web Share API**. If a player is on a phone, it will open their actual WhatsApp/Facebook share sheet. If they are on a PC, it copies the text to their clipboard. This makes the game "viral."
5.  **Bengali Language Support**: By using `family=Hind+Siliguri`, the game ensures that the Bengali text looks modern and clean, not like a default robotic font.
