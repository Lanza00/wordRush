# Word Rush - Malay to English Translation Game

An educational typing and translation game designed to help users improve their Malay to English vocabulary skills through an engaging, gamified experience.

## Overview

Word Rush is a web-based educational game that challenges players to translate English words to Malay as quickly and accurately as possible. The game features multiple difficulty levels, real-time feedback, streak tracking, and a competitive leaderboard system.

## Features

### Game Mechanics
- **4 Difficulty Levels**: Beginner, Intermediate, Advanced, and Expert vocabulary
- **10 Questions Per Game**: Each game session presents 10 randomly selected words
- **Lives System**: Players start with 3 lives; losing all lives ends the game
- **Time Challenge**: 120-second timer with time bonuses for correct answers
- **Streak System**: Build combos by answering 3+ questions correctly in a row

### User Experience
- **Countdown Animation**: "Get Ready! 3, 2, 1, GO!" countdown before each game
- **Audio Feedback**:
  - Correct answer sound (high-pitched tone)
  - Wrong answer sound (buzzer tone)
  - Streak achievement sound (ascending tones)
  - Countdown sounds with special "GO!" fanfare
- **Visual Feedback**: Color-coded word highlighting showing correct/incorrect matches
- **Progress Bar**: Visual indicator of game completion
- **Responsive Design**: Clean, modern UI that works on all devices

### Learning Features
- **Word-by-Word Scoring**: Partial credit for multi-word translations
- **Detailed Explanations**: Each word includes context and usage information
- **Answer Comparison**: Side-by-side view of user answer vs. correct answer

### Leaderboard System
- **Top 10 Rankings**: Track the best scores across all difficulty levels
- **Persistent Storage**: Scores saved in browser localStorage
- **Player Statistics**: View name, score, difficulty level, and date

## Technical Specifications

### Technology Stack
- **Frontend**: Pure HTML5, CSS3, JavaScript (ES6+)
- **Audio**: Web Audio API for dynamic sound generation
- **Storage**: Browser localStorage for leaderboard persistence
- **No Dependencies**: Completely standalone - no external libraries required

### File Structure
```
wordRush/
├── index.html          # Main game file (all-in-one)
├── logo.jpeg          # Game logo/branding
└── README.md          # This file
```

### Browser Compatibility
- Chrome/Edge (Chromium): ✓ Full support
- Firefox: ✓ Full support
- Safari: ✓ Full support
- Opera: ✓ Full support

## Installation

1. **Download/Clone** the repository
2. **Open** `index.html` in any modern web browser
3. **Start Playing!** No server or build process required

### Running Locally
```bash
# Option 1: Double-click index.html

# Option 2: Use a local server (optional)
cd wordRush
python -m http.server 8000
# Then open http://localhost:8000
```

## How to Play

1. **Choose Your Level**
   - 🟢 Level 1: Beginner Vocabulary (Car, Book, School...)
   - 🔵 Level 2: Intermediate Vocabulary (Knowledge, Experience, Decision...)
   - 🔴 Level 3: Advanced Vocabulary (Diagnosis, Treatment, Analysis...)
   - 🟣 Level 4: Expert Vocabulary (Serene, Fragile, Peculiar...)

2. **Game Start**
   - Watch for the countdown: "Get Ready! 3, 2, 1, GO!"
   - The timer starts immediately after

3. **Answer Questions**
   - Read the English word displayed
   - Type the Malay translation
   - Press Enter or click "Submit Answer"

4. **Scoring**
   - +10 points per correct word
   - +5 seconds per correct word
   - Build streaks for combo bonuses
   - Complete all 10 questions or run out of time/lives

5. **Save Your Score**
   - Enter your name
   - Click "Save Score"
   - Automatically return to main menu

## Vocabulary Database

### Level 1 (30 words)
Basic everyday vocabulary including common objects, actions, colors, and feelings.

### Level 2 (30 words)
Intermediate concepts covering abstract ideas, emotions, and common workplace/academic terms.

### Level 3 (30 words)
Advanced vocabulary from specialized fields: medical, legal, engineering, business, and psychology.

### Level 4 (30 words)
Expert-level rare and nuanced terms requiring deep vocabulary knowledge.

**Total Vocabulary**: 120 words with detailed explanations

## Game Logic

### Scoring System
```
Base Score: 10 points per correct word
Time Bonus: +5 seconds per correct word
Lives: 3 hearts (lose 1 for completely wrong answers)
Streak: Activated at 3+ consecutive correct answers
```

### Word Matching Algorithm
- Case-insensitive comparison
- Space-separated word matching
- Partial credit for multi-word answers
- Each word can only match once

### Game End Conditions
1. Complete 10 questions
2. Timer reaches 0
3. Lives reach 0

### Performance Ratings
- 900+ points: "🏆 Outstanding! Vocabulary Master!"
- 700-899 points: "⭐ Excellent! Great job!"
- 500-699 points: "👍 Good effort! Keep practicing!"
- 0-499 points: "📚 Keep learning! You can do better!"
- Out of lives: "💔 Game Over! You ran out of lives. Keep practicing!"
- Time's up: "⏰ Time's up! Better luck next time!"

## Customization

### Modifying Vocabulary
Edit the `vocabulary` object in `index.html` (around line 470):
```javascript
const vocabulary = {
    level1: [
        {
            en: "English Word",
            ms: "Malay Word",
            explanation: "Explanation text..."
        },
        // Add more words...
    ]
};
```

### Adjusting Game Settings
Modify these variables in the `startGame()` function:
```javascript
lives = 3;          // Starting lives
timeLeft = 120;     // Starting time (seconds)
```

### Changing Difficulty Colors
Edit the CSS classes in the `<style>` section:
```css
.btn-level1 { background: #00C853; } /* Green */
.btn-level2 { background: #2196F3; } /* Blue */
.btn-level3 { background: #ff0000c9; } /* Red */
.btn-level4 { background: #9C27B0; } /* Purple */
```

## Educational Benefits

- **Vocabulary Building**: Systematic learning across 4 proficiency levels
- **Active Recall**: Forces retrieval of information from memory
- **Immediate Feedback**: Learn from mistakes in real-time
- **Spaced Repetition**: Randomized questions support long-term retention
- **Contextual Learning**: Each word includes usage explanations
- **Gamification**: Makes language learning engaging and fun

## Future Enhancement Ideas

- [ ] Add more language pairs (English-Indonesian, English-Thai, etc.)
- [ ] Implement user accounts and cloud sync
- [ ] Add practice mode without timer/lives
- [ ] Include pronunciation audio
- [ ] Add achievement badges
- [ ] Create daily challenges
- [ ] Add multiplayer mode
- [ ] Export progress reports
- [ ] Mobile app version
- [ ] Difficulty adjustment based on performance

## Credits

**Game Design & Development**: Created for educational purposes

**Audio**: Web Audio API - dynamically generated sound effects

**Vocabulary**: Curated Malay-English translations with usage context

## License

This project is open for educational use. Feel free to modify and adapt for your language learning needs.

## Support

For questions, suggestions, or bug reports, please open an issue in the repository.

---

**Version**: 1.0.0
**Last Updated**: January 2026
**Language Pair**: Malay ↔ English
