# API-Driven Quiz App (Flutter)

## Overview

This project is a Flutter-based quiz application that retrieves live trivia questions from an external API and displays them dynamically. The app demonstrates the full API data flow: sending a request, receiving JSON, parsing the data into structured objects, and rendering it in an interactive user interface.

## Features

* Fetches trivia questions from the Open Trivia Database API
* Parses JSON into a structured Question model
* Displays multiple-choice questions dynamically
* Tracks user score and quiz progress
* Disables answer buttons after selection to prevent multiple inputs
* Provides immediate visual feedback:

  * Correct answers highlighted in green with a check icon
  * Incorrect selections highlighted in red with an X icon
* Decodes HTML entities for clean text display
* Allows users to restart the quiz or load a new set of questions

## Project Structure

```
lib/
├── main.dart            # App entry point
├── question.dart        # Data model for quiz questions
├── api_service.dart     # Handles API requests and JSON parsing
└── quiz_screen.dart     # UI and state management
```

## How It Works

1. The app sends a GET request to the trivia API.
2. The API returns a JSON response containing quiz data.
3. The data is parsed into Question objects.
4. The UI displays each question and answer choices.
5. User selections update the score and trigger visual feedback.

## Installation & Setup

1. Clone the repository:

```
git clone <your-repo-url>
cd <your-repo-folder>
```

2. Install dependencies:

```
flutter pub get
```

3. Run the app:

```
flutter run
```

## Dependencies

* http: Used to make API requests
* html_unescape: Used to decode HTML entities in API responses

## API Used

Open Trivia Database
https://opentdb.com/

Example endpoint:

```
https://opentdb.com/api.php?amount=10&category=9&difficulty=easy&type=multiple
```

## Enhanced Features

1. **Answer Feedback System**

   * Highlights selected answers with color-coded feedback
   * Displays icons indicating correct and incorrect selections

2. **Dynamic Question Reloading**

   * Users can generate a completely new set of questions at the end of the quiz

## Known Limitations

* No persistent storage (score resets after app restart)
* Limited customization of quiz categories/difficulty within UI
* Requires internet connection to fetch questions

## Author

Trajuan Smith
