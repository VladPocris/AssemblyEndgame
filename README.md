# Assembly Endgame

A fun and educational hangman-style game where you guess programming languages by revealing letters from randomly selected tech stack words. Each incorrect guess eliminates a language from your available options, with Assembly being the final language you need to learn to win!

## Description

Assembly Endgame is a React-based word guessing game built with Vite that challenges players to identify programming languages from partially revealed words. The game features:

- **Tech Stack Theme**: Words are drawn from popular programming languages and technologies
- **Progressive Elimination**: Each wrong guess removes a language from your available options
- **Visual Feedback**: Color-coded language cards show your progress
- **Celebration Effects**: Confetti animation when you win
- **Farewell Messages**: Custom messages for each eliminated language

## Features

- Responsive design that works on desktop and mobile
- Keyboard interaction for letter guessing
- Dynamic UI that updates based on game state
- Visual distinction between won/lost game states
- Configurable word lists and language data
- New game functionality to restart at any time

## Technologies Used

- **React 18** - Frontend library
- **Vite** - Build tool and development server
- **Canvas Confetti** - Celebration animations
- **CSS3** - Styling and animations
- **JavaScript (ES6+)** - Programming language

## Installation

1. Clone the repository:
```bash
git clone https://github.com/VladPocris/assembly-endgame.git
```

2. Navigate to the project directory:
```bash
cd assembly-endgame
```

3. Install dependencies:
```bash
npm install
```

4. Start the development server:
```bash
npm run dev
```

5. Open your browser and visit `http://localhost:5173` (or the URL shown in your terminal)

## How to Play

1. The game displays a series of underscores representing letters in a hidden programming language word
2. Click on the on-screen keyboard or use your physical keyboard to guess letters
3. Correct guesses reveal the letter in all its positions in the word
4. Incorrect guesses eliminate a language from your available options (shown at the bottom)
5. The game ends when you either:
   - **Win**: Guess all letters in the word before running out of languages
   - **Lose**: Eliminate all languages (reach Assembly as your last option)
6. Click "New game" to play again with a different word

## Game Mechanics

- You start with all programming languages available
- Each incorrect guess removes one language from your options (in order: HTML, CSS, JavaScript, React, TypeScript, Node.js, Python, Ruby, Assembly)
- When you lose, the last eliminated language determines your "farewell" message
- Winning triggers a confetti celebration
- The word list includes various programming languages, frameworks, and technologies

## Project Structure

```
src/
├── App.jsx                 # Main application component
├── index.jsx               # Entry point
├── index.css               # Global styles
├── languages.js            # Language data with colors
├── words.js                # Word list for the game
├── utils.js                # Helper functions
└── components/
    ├── Header.jsx          # Game title
    ├── GameStatus.jsx      # Win/lose/farewell messages
    ├── Languages.jsx       # Display of available/eliminated languages
    ├── GuessWord.jsx       # Word display with guessed letters
    └── Keyboard.jsx        # On-screen keyboard
```

## Customization

### Modifying the Word List
Edit `src/words.js` to add or remove words from the game:
```javascript
export const words = [
  "HTML",
  "CSS", 
  "JavaScript",
  // Add your words here
];
```

### Changing Languages
Edit `src/languages.js` to modify the languages, their order, or colors:
```javascript
export const languagesData = [
  {
    name: "HTML",
    backgroundColor: "#E2680F",
    color: "#F9F4DA",
  },
  // Modify or add languages here
];
```

### Adjusting Game Difficulty
Change the number of allowed wrong guesses by modifying the languages array length in `App.jsx`:
```javascript
const isGameLost = wrongGuessCount >= languagesData.length - 1;
```

## Building for Production

To create a production build:
```bash
npm run build
```

The built files will be in the `dist/` directory, ready for deployment.

## Preview

Live -> (https://assembly-endgame-khaki-iota.vercel.app/)

## License

This project is open source and available under the [MIT License](LICENSE).

---

## CV Section

### Vlad Pocris - Software Developer

**Assembly Endgame** - React/Vite Programming Language Game
- Developed an interactive hangman-style game teaching programming languages through word guessing
- Implemented React hooks (useState, useEffect) for dynamic state management
- Created responsive UI with keyboard interaction and visual feedback systems
- Integrated canvas-confetti for celebratory animations on win conditions
- Designed progressive elimination mechanic where incorrect guesses remove language options
- Built reusable components (Header, GameStatus, Languages, GuessWord, Keyboard) following React best practices
- Utilized Vite for fast development builds and optimized production bundling
- Applied CSS modules and modern JavaScript (ES6+) for clean, maintainable code
- Implemented game logic with win/lose conditions and custom farewell messages per eliminated language
- Deployed responsive design ensuring compatibility across desktop and mobile devices

**Key Technologies**: React, Vite, JavaScript (ES6+), CSS3, Canvas Confetti
**Concepts Demonstrated**: State management, component architecture, event handling, responsive design, game development principles
