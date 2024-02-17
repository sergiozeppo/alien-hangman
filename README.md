This is my implementation of RS School task 'hangman' 
https://github.com/rolling-scopes-school/tasks/tree/master/stage1/tasks/hangman

### Project's Description

[Hangman](<https://en.wikipedia.org/wiki/Hangman_(game)>) is a classic word game in which you must find the correct answer by guessing letters one at a time.

### Game rules

1. The game is represented by two main parts: **the gallows part** and **the quiz part**.
2. At the beginning of the game, the gallows **is empty**.
3. The quiz part includes:

- a question,
- a secret word (the answer to the question), represented by underscores **for each** letter in the word _(for example, if the secret word is 'address' it will be written like '\_ \_ \_ \_ \_ \_ \_')_,
- an incorrect guesses counter,
- a virtual keyboard,

4. The user must be able to use **both virtual** _(by clicking letter keys on the screen)_ and **physical keyboards** _(by pressing letter keys on their keyboard)_ to play the game.
5. When the user starts guessing the letters:

- whenever the letter is guessed correctly, this letter appears **instead of the corresponding underscore(s)** _(for the example mentioned above, if the user clicks or presses the 'd' letter, both 'd's must appear on the screen: '\_ d d \_ \_ \_ \_')_;
- if the letter is not in the word, **one body part** must be added to the gallows and the incorrect guesses counter **must be updated** accordingly;
- the clicked/pressed letter **must be disabled** and it must be reflected in the UI _(for example, by using a different color on the disabled button)_;

6. The body parts appear on the gallows in the **following order**: head, body, left arm, right arm, left leg, right leg. It means that the user has **6 attempts** to guess the word.
7. The player will continue guessing letters until either **the word is solved** or **all six body parts** are on the gallows.
8. At the end of the game, a **modal window** must appear. It must:

- include the **message** that either congratulates the user on winning the game or informs them that they failed to win;
- the **secret word** (even if it was guessed correctly);
- a **"play again"** button.

9. When the user clicks on "play again", the game **starts over**:

- the gallows is **empty**;
- the question is **changed**;
- the underscores are **updated** according to the new secret word _(the same secret word can't be used as an answer to more than one question)_;
- an incorrect guesses counter is **set to 0**.

### Approximate appearance

_This example is purely illustrative. Feel free to change the layout as you wish._
![screenshot](hangman.png)

### Helpful materials

At the [following link](https://www.figma.com/file/ug2NAUiXPpaFDvch5TWUxd/Hangman-game?type=design&node-id=0%3A1&mode=design&t=4Gj7Ayo0yckppNo8-1) you will find:

- examples of the game flow,
- body parts (for those who don't want to design them by themselves).

### Main functional requirements

- The design must be **adaptive (or responsive)**, that includes desktop(1440px <= width), tablet(768px <= width < 1440px) and mobile(360px <= width < 768px). When switching between versions everything must be displayed correctly, all functionality must be present, no content must disappear or be left beyond the screen.
- Initially, `body` in the `index.html` file **must be empty**, all necessary elements are generated using JS.
- Both at the beginning and in the end of the game, the question-answer pair must be **chosen randomly** _(it's recommended to have at least 10 question-answer pairs)_.
- The application can be done **in English or in Russian**.

### Additional functionality added by me beyond main functional requirements
- I have chosen to hang an **Alien**, so implemented this beautiful design
- I recorded a sounds of **Alien crying**.
- I added a **UFO-like soundtrack** and a **button to switch sounds on/off**

## Technical requirements

- The application is displayed correctly and functions properly in the latest version of Google Chrome.
- It is **not allowed** to use:
  - CSS frameworks (e.g., `Bootstrap`),
  - JS frameworks (e.g., `Angular`, `React`, `Vue`, etc.),
  - Outdated libraries (e.g. `JQuery`, etc.),
  - Any JS libraries which are not devDependencies (e.g. `lodash`),
  - `TypeScript`.
- You can use CSS preprocessors (`SASS`, `SCSS`) and `normalize.css`.
- It is strongly recommended to use `eslint` and `prettier`.
