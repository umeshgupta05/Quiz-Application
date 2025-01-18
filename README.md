# Quiz Application

A flexible, interactive quiz application built with jQuery and AJAX that loads questions from XML and supports dynamic option editing.

## Features

- XML-based question management
- Dynamic option editing during quiz
- Detailed final results with question-by-question review
- Progress tracking
- Navigation between questions
- Immediate feedback on answers
- Responsive design
- Score calculation and statistics
- Quiz restart functionality

## Installation

1. Clone the repository or download the files:
```bash
git clone https://github.com/yourusername/dynamic-quiz-app.git
cd dynamic-quiz-app
```

2. Set up the file structure:
```
quiz/
├── quiz.html
├── questions.xml
└── README.md
```

3. Deploy to a web server (required for AJAX functionality)
   - You can use any web server like Apache, Nginx, or even PHP's built-in server
   - For local development with PHP:
     ```bash
     php -S localhost:8000
     ```

## File Structure

### quiz.html
Contains the main application code including HTML, CSS, and JavaScript.

### questions.xml
Stores quiz questions in XML format. Example structure:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<quiz>
    <question id="1">
        <text>What is jQuery?</text>
        <options>
            <option>A programming language</option>
            <option>A JavaScript library</option>
            <option>A database</option>
            <option>A web server</option>
        </options>
        <correct>1</correct>
    </question>
    <!-- Add more questions here -->
</quiz>
```

## Usage

### Taking the Quiz
1. Open the application in a web browser
2. Click through questions using Next/Previous buttons
3. Select answers by clicking on options
4. View immediate feedback after selecting an answer
5. See detailed results at the end
6. Option to restart quiz when finished

### Editing Options
1. Click "Edit Options" button while viewing a question
2. Edit text for any option in the input fields
3. Click "Save Options" to confirm changes
4. Continue with the quiz

### Adding New Questions
1. Open `questions.xml`
2. Add new question blocks following the XML structure:
```xml
<question id="[unique_id]">
    <text>[Your question text]</text>
    <options>
        <option>[Option 1]</option>
        <option>[Option 2]</option>
        <option>[Option 3]</option>
        <option>[Option 4]</option>
    </options>
    <correct>[Correct option index (0-based)]</correct>
</question>
```

## Customization

### Styling
The application uses custom CSS classes that can be modified in the `<style>` section of index.html:
- `.quiz-container`: Main container styling
- `.option`: Question option styling
- `.correct`: Correct answer highlighting
- `.incorrect`: Incorrect answer highlighting
- `.question-review`: Results page question review styling

### Adding Features
Common extension points:
1. Timer functionality:
   - Add a timer variable in the JavaScript
   - Create a display element in the HTML
   - Update the timer in an interval

2. Question categories:
   - Add a `category` tag in the XML
   - Modify the parsing function to include categories
   - Add category filtering UI

3. Different question types:
   - Add a `type` attribute in the XML
   - Create new display functions for each type
   - Modify the question display logic

## Dependencies

- jQuery 3.7.1
- Web server (for AJAX functionality)
- Modern web browser with JavaScript enabled

## Known Issues

1. Changes to options are not persistent after page refresh
2. No server-side validation of answers
3. Limited to single-choice questions

## Future Improvements

1. Server-side storage for edited options
2. Multiple question types (multiple choice, true/false, etc.)
3. User authentication and score tracking
4. Question categories and filtering
5. Time limits per question
6. Export results functionality
