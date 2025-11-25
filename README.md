# Slot Machine
## Online Casino Game

![Slot Machine](https://raw.githubusercontent.com/1stake/assets/b3e211525769c4a704ec775708fff66c70dc07f9/slot-machine-online-casino-game-plugin.webp)

### 🎰 Overview
An HTML5 / JavaScript slot machine game that lets users spin and win like in a real **online casino**, but without real money. 
Embed it easily into any website with zero server dependencies.

### ✨ Key Features
- 🧩 5 Reels & 20 Paylines
- 🃏 Wild symbol support
- 🌟 Scatter symbol support
- 🎚 Adjustable bet amount & selectable lines each round
- 💾 Balance persistence via local browser storage
- ⚙️ Fully customizable (default bet, max bet, lines, symbols, reels, payouts)
- 🌐 Multi-language support
- 🚀 Pure client-side: runs from a single index.html
- 🔌 Easy embedding into existing layouts

### 🚀 Quick Start
1. Download the latest build.
2. Open `index.html` in any modern browser.
3. Start spinning! 🔄

### 🔗 Minimal Integration Example
Embed inside your page (adjust paths as needed):
```html
<!DOCTYPE html>
<html lang="en">  
  <link rel="stylesheet" href="assets/css/main.css">
  <script src="assets/js/main.js"></script>
</head>
<body style="width:100vw;height:100vh;margin:0;padding:0;">
  <div id="slot-machine"></div>
</body>
</html>
```

### ⚙️ Configuration Options
It is possible to override the default configuration by passing a custom `slotMachineConfig` object when initializing the game.

Example:
```html
<script>
var slotMachineConfig = {
  minBet: 1,
  maxBet: 100,
  defaultBet: 1,
  betChangeAmount: 1,
  lineCount: 20,
  balance: 500,
  symbols: [
    {
      filename: 'symbol.png',
      scatter: false,
      wild: false,
      w1: 0, // payout for 1 symbol on a line
      w2: 0, // payout for 2 symbols on a line
      w3: 5, // payout for 3 symbols on a line
      w4: 10, // payout for 4 symbols on a line
      w5: 20 // payout for 5 symbols on a line
    },
    ...
      {
        filename: 'wild.png',
        scatter: false,
        wild: true, // this symbol acts as a wild
        w1: 0, // wilds typically don't have payouts
        w2: 0, 
        w3: 0,
        w4: 0,
        w5: 0
      },
    {
      filename: 'scatter.png',
      scatter: true, // this symbol acts as a scatter
      wild: false,
      w1: 0, // payout for 1 symbol everywhere
      w2: 2, // payout for 2 symbols everywhere
      w3: 5, // payout for 3 symbols everywhere
      w4: 10, // payout for 4 symbols everywhere
      w5: 20 // payout for 5 symbols everywhere
    }
  ],
  reels: [
    // Each sub-array represents a reel with symbol indices.
    // There should be exactly 5 reels.
    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
    [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 0],
    [2, 3, 4, 5, 6, 7, 8, 9, 10, 0, 1],
    [3, 4, 5, 6, 7, 8, 9, 10, 0, 1, 2],
    [4, 5, 6, 7, 8, 9, 10, 0, 1, 2, 3]
  ],
  // i18n support
  textStrings: {
    'Balance': 'Stand', // original --> translation
    'Bet': 'Wette',
    ... // other text strings
  },
};
</script>
````
Custom configuration options should be defined before loading `main.js`.

### 🛡 Disclaimer
This is a free, **virtual slot machine** for entertainment & educational purposes. 
No real wagers, no cash-out, no gambling functionality.

### 📄 License
This project is licensed under the [MIT License](LICENSE).

Enjoy spinning! 🎰
