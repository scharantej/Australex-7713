## Flask Application Design

### HTML Files

- `index.html`: The main HTML file that displays the flashcards and their translations.
  - Content:
    - A navigation bar with a link to the translation form.
    - A section to display the flashcards, each with a title and translation.
    - A form to submit new flashcards for translation.
- `translate.html`: A form to submit new flashcards for translation.
  - Content:
    - A title for the form.
    - Two input fields, one for the title and one for the translation.
    - A submit button.

### Routes

- `/`: The main route that displays the flashcards.
  - Method: GET
  - Function:
    - Retrieves the flashcards from the database.
    - Renders the `index.html` template with the flashcards.
- `/translate`: The route that handles the submission of new flashcards.
  - Method: POST
  - Function:
    - Extracts the title and translation from the request form.
    - Saves the new flashcard to the database.
    - Redirects to the main page `/`.