# Assembly: Endgame

A word-guessing survival game built with React where players race to guess a hidden programming-related word before Assembly takes over the stack.

## Overview

In **Assembly: Endgame**, each wrong guess eliminates one programming language in sequence—starting from HTML and working down toward Assembly—until you either solve the word or run out of attempts. Winning triggers a confetti celebration, while losing reveals any missed letters and ends the round with a **New Game** reset option.

## Features

- **Word Guessing Gameplay:** Guess letters interactively via an on-screen keyboard (`A`–`Z`) with visual feedback for correct and incorrect guesses.
- **Language Survival Progression:** Visual status updates across languages (`HTML`, `CSS`, `JavaScript`, `React`, `TypeScript`, `Node.js`, `Python`, `Ruby`, and `Assembly`) as incorrect attempts accumulate.
- **Win & Loss States:**
  - Celebrates wins with `react-confetti`.
  - Reveals missed letters on a loss and disables further keyboard input once the game ends.
- **One-Click Replay:** Reset state and start a fresh round immediately with the **New Game** button.
- **Accessibility Support:** Includes live status updates, `aria-label` attributes on letter keys, and `aria-disabled` states.

## Tech Stack

- **React** (`18.3.1`) & **React DOM** (`18.3.1`)
- **clsx** (`2.1.1`) for conditional class names
- **react-confetti** (`6.1.0`) for win celebrations
- **CSS** (`index.css`) for layout, states, and responsive styling

## Project Structure

```text
├── App.jsx          # Main game state, derived win/loss/keyboard logic, and UI
├── index.jsx        # Application entry point
├── index.html       # Base HTML template
├── index.css        # Styling for board, keyboard, status banner, and buttons
├── languages.js     # Programming language list and metadata
├── utils.js         # Helper utilities (e.g., word selection and farewell/status messages)
└── words.js         # Target word bank
