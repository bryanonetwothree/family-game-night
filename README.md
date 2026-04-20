# 🀄 家庭遊戲夜 · Family Game Night

A fun, offline-ready family party game for Cantonese-speaking families. No app store, no install, no internet required — just open the HTML file on any phone or tablet and play!

---

## 🎮 How to Play

1. **Enter family member names** — add everyone who's playing
2. **Card Draw** — a glowing frame bounces between the cards and picks the unlucky one 😬
3. **Game Pick** — one of 3 mini-games is randomly selected for that person
4. **Keep going** — repeat rounds as long as you want
5. **Quit anytime** — a wrap-up screen shows who got picked the most (今日最衰仔/女 🏆)

---

## 🎲 Current Games

| # | Game | Description |
|---|------|-------------|
| 🎭 | **成語比手畫腳** | The chosen person gets a random 成語 (Chinese idiom). Others close their eyes, then guess from actions only — no sounds, no pointing at words! |
| 👅 | **急口令挑戰** | Recite a Cantonese tongue twister 3 times fast without stumbling. Family votes pass 👍 or fail 👎 — losers do 10 squats! |
| 🎪 | **模仿大挑戰** | Impersonate a randomly assigned family member for 30 seconds. Family rates 1–5. Score 4+ and you get to dare anyone in the room 😈 |

---

## 🚀 Getting Started

No installation needed.

```
1. Download family_game_night.html
2. Open it in any mobile browser (Safari, Chrome, etc.)
3. Gather the family and start!
```

Works fully offline after the first load (Google Fonts loads once on first open).

---

## 🤝 Contributing — Add More Games & Varieties!

**The current game variety is intentionally small — this project is open for everyone to expand!**

Whether you want to add new mini-games, more 成語, more tongue twisters, or support for other languages/dialects, contributions are very welcome.

### Ideas for contributions

- 🃏 New mini-games (drinking game variants, drawing challenges, trivia...)
- 📝 More 成語 to the charades list
- 👅 More 急口令 (tongue twisters in Cantonese, Mandarin, English...)
- 🌍 Translations / localisation for other families (Mandarin, English, etc.)
- 🎨 UI themes (e.g. New Year red, Halloween, birthday party)
- 🔊 Sound effects
- 📊 Better score tracking across sessions

### How to add a new game

All games live in the `GAMES` array inside the `<script>` tag. Each game object follows this structure:

```javascript
{
  id: 3,                        // next available index
  emoji: '🎯',                  // shown on the game card
  name: '你的遊戲名',            // game card label
  render(winner, players) {     // called when this game is picked
    return `<div class="game-box">
      <div class="game-box-title">🎯 遊戲四 · 你的遊戲名</div>
      <!-- your game content here -->
    </div>`;
  }
}
```

Then add your emoji and label to `GAME_EMOJIS` and `GAME_LABELS` arrays, and update the game cards grid in the HTML to show 4 cards instead of 3.

### How to add more 成語

Find the `CHENGYUS` array and add your entries:

```javascript
const CHENGYUS = [
  '一箭雙鵰', '一毛不拔', // ... existing ones
  '馬到成功',             // ← add yours here
];
```

### How to add tongue twisters

Find the `TWISTERS` array:

```javascript
const TWISTERS = [
  { txt: '你的急口令', hint: '快速重複三次不出錯' },
];
```

---

## 📁 Project Structure

```
family_game_night.html    ← the entire app, single file
README.md
```

Everything — HTML, CSS, and JavaScript — lives in one self-contained file, making it easy to share via WhatsApp, AirDrop, or just dropping it in a group chat.

---

## 🌟 Inspired By

Built for Cantonese families during 清明節 (Tomb Sweeping Day) gatherings, where no one could agree on what to do after dinner 😄. Designed to be picked up and played with zero setup by grandparents and kids alike.

---

## 📄 License

MIT — free to use, share, and modify. If you make a fun version for your family, consider sharing it back!
