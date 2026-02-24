All code courtesy of Claude.ai

# 🎲 2d6 Distribution Tracker

A webpage for tracking the probability of dice rolls and comparing it to expected data. Perfect for settling Catan disputes about luck. Loosely based off Colonist dice results.

---

## Overview

When you roll two six-sided dice, the possible sums range from 2 to 12. Because of how probabilities combine, these sums don't occur equally — a result of **7 is six times more likely** than a 2 or 12. Over time, the distribution of results should form a classic bell curve.

This tool lets you log each roll in real time and see exactly how closely (or how wildly) your actual results match that theoretical expectation.

---

## Getting Started

No installation required. Just open `dice-tracker.html` in any modern web browser.

```
1. Download dice-tracker.html
2. Double-click the file to open it in your browser
3. Start clicking your roll results to record them
```

---

## Features

### 📊 Live Bell Curve Chart
- A gold overlay shows the **theoretical expected distribution** for 2d6
- Bars update in real time as you log rolls
- **Green bars** = you've rolled this value more than expected
- **Red bars** = you've rolled this value less than expected

### 📋 Deviation Table
For every possible result (2–12), the table shows:
- **Observed count** — how many times you've rolled it
- **Expected %** — the theoretical probability
- **Observed %** — your actual frequency so far
- **% Deviation** — signed difference from expected (+ or −)
- **Mini bar** — visual proportion of your rolls

### 📈 Session Stats
- Total rolls recorded
- Observed mean vs. the expected mean of **7**
- Mode (most frequently rolled value)
- Average absolute deviation across all values

### Controls

| Button | Action |
|---|---|
| **Roll buttons (2–12)** | Record a roll result |
| **↩ Undo Last** | Remove the most recent entry |
| **✕ Clear All** | Reset all data and start over |
| **⚄ Simulate 100** | Auto-generate 100 random rolls to demo the curve |

---

## The Math Behind It

For two six-sided dice, the number of ways to roll each sum:

| Sum | Ways to roll | Probability |
|-----|-------------|-------------|
| 2   | 1           | 2.78%       |
| 3   | 2           | 5.56%       |
| 4   | 3           | 8.33%       |
| 5   | 4           | 11.11%      |
| 6   | 5           | 13.89%      |
| 7   | 6           | 16.67%      |
| 8   | 5           | 13.89%      |
| 9   | 4           | 11.11%      |
| 10  | 3           | 8.33%       |
| 11  | 2           | 5.56%       |
| 12  | 1           | 2.78%       |

The expected mean is **7**, and the distribution is perfectly symmetrical around it.

---

## Use Cases

- Board game sessions — track dice luck over a long game
- Tabletop RPGs — verify whether your dice are rolling fairly
- Statistics education — demonstrate the law of large numbers in action
- Just curious whether your dice are cursed

---

## Technical Details

- **Pure HTML/CSS/JavaScript** — no frameworks, no dependencies, no internet connection required after opening the file
- Chart rendered on an HTML5 `<canvas>` element
- Fully responsive — works on desktop and mobile browsers
- All data is stored in memory; refreshing the page resets your session

---

## License

Free to use, modify, and share.
