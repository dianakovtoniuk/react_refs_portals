# Timer Challenge

A small browser game built with React. Enter your name, pick a challenge and try to stop the timer as close to zero as possible without letting it run out.

## Features

- Player name input that updates the welcome message
- Several timer challenges with different target times
- Start and stop controls with a live active state indicator
- Result dialog showing the target time, the time left and a score
- Automatic loss when the timer reaches zero

## How It Works

The score is calculated from how much time was left when you stopped the timer compared to the target time. The closer you stop to zero, the higher the score. If the time runs out, the game is lost.

## Tech Stack

- React
- Native HTML dialog element
- React portals
- Plain CSS

## React Concepts Used

- Refs for reading input values and storing timer IDs
- State for tracking the remaining time
- Forwarded refs with an imperative handle to open the result dialog from the parent component
- Portals to render the dialog into a separate DOM node
- Derived values calculated during rendering instead of extra state

## Getting Started

### Prerequisites

- Node.js 18 or newer
- npm

### Installation

1. Clone the repository with `git clone https://github.com/dianakovtoniuk/react.git`
2. Go to the project folder with `cd react`
3. Install dependencies with `npm install`
4. Start the development server with `npm start`

The app will be available at http://localhost:3000.

## Project Structure

- `public/` static files and the HTML template, including the `modal` container used by the dialog
- `src/`
  - `components/`
    - `Player.jsx` player name input and greeting
    - `TimerChallenge.jsx` timer logic and controls for a single challenge
    - `ResultModal.jsx` dialog with the result, rendered through a portal
  - `App.jsx` root component
  - `index.jsx` application entry point
  - `index.css` global styles
