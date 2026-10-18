# Chingu Trivia — Product Owner Solo Project

## Product overview

Chingu Trivia is a browser-based quiz app. Players answer multiple-choice and true/false questions, receive feedback, and see their final score. They can choose a subject and return later without repeating answered questions until they clear their progress.

**Product goal:** Help players practise their knowledge, understand their results, and continue through the available questions across multiple visits.

**Main user:** A learner who wants to practise a subject and check their knowledge.

## Epic 1: Display the quiz

Let the player open the app, see questions, and understand their progress.

### User story 1: See the app name

As a player, I want to see the app name so that I know which app I am using.

**Tasks:**

- Add a header showing “Chingu Trivia.”
- Add tabs only if the design uses them.

### User story 2: See a question and answer choices

As a player, I want to see a question with answer choices so that I can select my answer.

**Tasks:**

- Display each question in a card.
- Support multiple-choice and true/false questions.
- Display the choices clearly and allow the player to select one answer.
- Load questions from the source provided below.
- Make all supplied questions available while following the no-repeat rule in Epic 4.

**Question source:** https://johnmeade-webdev.github.io/chingu_quiz_api/trial.json

### User story 3: Start the quiz and see my position

As a player, I want to see the first question and my position so that I know where to begin and how far I have progressed.

**Tasks:**

- Display the first question when a new quiz begins.
- Display the current question number and total, for example “Question 1 / 10.”
- Update the current question number when the player moves forward.
- Make sure the displayed total matches the agreed quiz length.

**Question for clarification:** The brief says to cover all questions but also gives “Question 1 / 10.” Should each quiz contain 10 questions, or should the total reflect all available questions?

---

## Epic 2: Answer questions and see results

Let the player receive feedback, move forward, and see their final score.

### User story 4: Know whether my answer is correct

As a player, I want feedback after submitting an answer so that I know whether I answered correctly.

**Tasks:**

- Check the submitted answer against the correct answer.
- Display a clear correct or incorrect message.
- Count correct answers for the final score.
- Make sure the same answer is not counted more than once.

### User story 5: Move to the next question

As a player, I want to move to the next question after answering so that I can continue the quiz.

**Tasks:**

- Add a Next question button.
- Keep it hidden or disabled until the current answer is submitted.
- Make it available after submission.
- Display the next question when the player selects it.
- Show the next question without reloading the whole page.

### User story 6: See my final score

As a player, I want a completion message and my score so that I know how I performed.

**Tasks:**

- Recognise when the final question has been answered.
- Show a clear message that the quiz is complete.
- Show correct answers out of the total, for example “You answered 7 out of 10 correctly.”
- Check that the score matches the submitted answers.

---

## Epic 3: Choose questions by subject

Let the player answer questions about a subject they choose.

### User story 7: Choose a subject

As a player, I want to choose a subject so that I can answer questions about an area that interests me.

**Tasks:**

- Identify the subjects in the supplied question source.
- Provide a clearly labelled subject selector.
- Display questions belonging to the chosen subject.
- Update the question counter to match the quiz for that subject.
- Continue excluding previously answered questions unless progress is cleared.

**Question for clarification:** Can players change subjects during a quiz, or only before starting? What should happen to the current quiz if they change subjects?

---

## Epic 4: Remember and clear progress

Let the player return without repeating answered questions and choose when to start again.

### User story 8: Avoid repeated questions across visits

As a returning player, I want the app to remember questions I have answered so that I receive questions I have not answered before.

**Tasks:**

- Record which questions the player has answered.
- Save progress using a backend, as required by the brief.
- Retrieve the saved progress when the player returns.
- Exclude previously answered questions until progress is cleared.
- Apply this rule even when the player changes subjects.
- Show a clear message when no unanswered questions remain.

**Question for clarification:** How should the app recognise a returning player? The brief does not specify whether an account is needed.

### User story 9: Clear my progress

As a player, I want to clear my progress so that I can answer the questions again.

**Tasks:**

- Provide a clearly labelled Clear progress action.
- Explain that clearing progress makes previously answered questions available again.
- Clear the saved record of answered questions when the player chooses this action.
- Make those questions available again.

---

## Epic 5: Make the quiz easy to use on different screens

Keep the quiz readable and its controls understandable on phones and computers.

### User story 10: Use the quiz on a small screen

As a player using a phone, I want the quiz to fit my screen so that I can read questions and select answers comfortably.

**Tasks:**

- Adjust the layout for small and large screens.
- Stack answer choices vertically on small screens.
- Keep text and controls inside the screen width.
- Avoid unnecessary scrolling while keeping all content accessible.
- Check that the quiz works on a small phone screen.

### User story 11: Understand the buttons and messages

As a player, I want clear buttons and messages so that I know what I can do next.

**Tasks:**

- Use clearly labelled buttons.
- Make unavailable buttons visibly disabled if they are displayed.
- Make feedback messages easy to understand.
- Keep the design clean and similar to the supplied demo references.
- Make sure styling changes do not make the quiz harder to use.

---

## Additional task: Check for errors before submission

**Tasks:**

- Check the browser’s developer console for errors while using the app.
- Fix errors found before submitting the app.
- Confirm that normal quiz actions do not reload the whole page.
