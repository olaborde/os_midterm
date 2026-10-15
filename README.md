# CGS1700 Operating Systems Midterm Review

**Study the concepts. Test your recall. Take the hot seat.**

An interactive operating systems review for CGS1700 students, created by **Osse Laborde**. Practice with a Millionaire-style quiz, run a classroom team competition, or work through flashcards at your own pace.

The review includes **50 questions across five study areas**, with correct answers and plain-language explanations.

[Open the review website](https://olaborde.github.io/os_midterm/) · [View the repository](https://github.com/olaborde/os_midterm)

> The website link works after GitHub Pages has been enabled and deployment has completed.

## Choose how you study

| Mode | What to expect |
| --- | --- |
| **Classroom review** | Answer all 50 questions or focus on one topic. Play solo or with up to six teams taking turns. |
| **Millionaire challenge** | Answer 15 questions, three from each study area, and climb the fictional money ladder. |
| **Flashcards** | Recall an answer before revealing it. Mark cards “Got it” or “Review again” and revisit your difficult cards. |

## Topics covered

| Study area | Main concepts |
| --- | --- |
| Computer and registers | Computer structure, instruction cycle, PC, IR, MAR, MBR, cache, multiprocessing |
| Interrupts and I/O | Interrupt handlers, processor state, ready signals, interrupt-driven I/O, DMA, DSP |
| Memory and addressing | Logical and physical addresses, fragmentation, compaction, best-fit, next-fit, overlays, protection |
| Concurrency tools | Critical sections, mutual exclusion, race conditions, semaphores, busy waiting, monitors, starvation |
| Threads and deadlocks | Process versus thread, thread states, user and kernel threads, deadlock conditions and handling |

## How to play

1. Choose **Classroom review** or **Millionaire challenge**.
2. Set the timer and enter your contestant or team names. Classroom review also offers topic filtering and question shuffle.
3. Read the question, discuss your reasoning, and select A, B, C, or D.
4. Choose **Final answer** to lock your choice.
5. Read the explanation before moving on.

Question timers can be set to **30, 45, or 60 seconds**, or turned off. Projector view enlarges the questions and answer choices. The game pauses when you switch tabs.

### Scoring

**Classroom review:** A correct answer earns **100 points**. An incorrect answer or timeout earns **0 points**. Teams alternate turns, and the review continues after a miss. Results include team scores, answer review, practice for missed questions, and CSV export.

**Millionaire challenge:** Each correct answer advances the bank to the next ladder value. One wrong answer ends the run and pays the last earned safety net:

| Milestone | Guaranteed bank |
| --- | ---: |
| Before five correct answers | $0 |
| Five correct answers | $1,000 |
| Ten correct answers | $32,000 |
| Fifteen correct answers | $1,000,000 |

Choose **Walk away** before locking an answer to keep your current bank. Classroom points and challenge dollars are separate fictional scores.

### Lifelines

Each team receives one use of each lifeline per game:

- **50:50:** Removes two incorrect choices.
- **Ask the Class:** The host enters actual classroom vote counts. Votes represent class opinions and may be incorrect.
- **Phone a Friend:** Gives 30 seconds to consult a classmate or another team while the question timer pauses.

## Study with flashcards

Choose **Study with flashcards** on the home screen.

1. Read the question and try to answer it from memory.
2. Click the card to reveal the correct answer and explanation.
3. Choose **Review again** or **Got it** to save your rating and advance.
4. Filter by topic, shuffle the deck, or enable **Review again only** to focus on difficult cards.

You can navigate without rating a card. At the end of a pass, study the topic again or revisit your review pile. Flashcard progress saves separately from quiz scores. **Reset flashcard progress** clears flashcard ratings after confirmation.

## Keyboard controls

| Action | Game | Flashcards |
| --- | --- | --- |
| Select an answer | A–D | — |
| Lock answer or continue | Enter | — |
| Reveal or hide an answer | — | Space or Enter on the card |
| Pause or resume | Space | — |
| Previous or next card | — | Left or right arrow |
| Mark “Review again” | — | 1, after revealing |
| Mark “Got it” | — | 2, after revealing |
| Toggle sound | M | M |
| Fullscreen | F | F |
| Close a dialog | Escape | Escape |

Buttons and form controls also support keyboard navigation. Use **Tab** to move between controls.

## Sound and display

Click **Sound off** in the header to enable sound. Browsers require a user interaction before audio can start. The game uses original synthesized cues for selections, correct answers, misses, and wins, plus optional suspense audio.

Open **?** for instructions and sound volume. Use **Fullscreen** for classroom projection. Layouts adapt to desktop and mobile screens, with reduced-motion styling when requested by the device.

## Run locally

For the single-file edition, save the application as **`index.html`** and open it in a modern browser. The file contains the HTML, styles, question bank, and JavaScript, so no build step or API key is needed.

For more consistent browser storage behavior, serve the folder locally:

```bash
git clone https://github.com/olaborde/os_midterm.git
cd os_midterm
python3 -m http.server 8000
```

Then visit [http://localhost:8000](http://localhost:8000).

If you are using the separate source bundle with its `dist/` folder, open `dist/index.html` or serve it with `python3 -m http.server 8000 --directory dist` instead.

## Deploy with GitHub Pages

For a single-file deployment:

1. Place **`index.html`** in the repository root.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the branch containing the file, usually **`main`**, and **`/ (root)`**.
5. Click **Save** and wait for deployment to finish.
6. Open the address shown in the Pages settings.

The expected project address is **https://olaborde.github.io/os_midterm/**. Committing a replacement `index.html` publishes subsequent updates through the configured Pages deployment.

[GitHub Pages setup documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

## Saved progress and results

Quiz sessions and flashcard ratings use the browser's **localStorage**. Progress belongs to the browser and website address where you study. It does not automatically sync across devices, browsers, or the offline and hosted versions.

Use **Export results** to download quiz results as a CSV. Starting a new quiz replaces the saved quiz session. Clearing browser storage removes saved progress.

Team play happens on a shared screen. This version does not provide remote multiplayer, a shared online leaderboard, or automatic instructor collection of student results.

## Editing and testing

In the single-file edition, edit the embedded `QUESTION_BANK` records in `index.html`. Each record contains an ID, category, question, four options, a zero-based correct-answer index, and an explanation.

Keep IDs unique and update the answer index whenever you reorder options. The Millionaire challenge expects five categories with at least three questions each.

If you have the full source bundle, question records live in `dist/questions.js`. The bundle also includes game and flashcard rule tests, which run with Node.js 20 or newer:

```bash
node --test tests/*.test.cjs
```

## Course information

**Course:** CGS1700 — Introduction to Operating Systems  
**Instructor:** Osse Laborde

This is a study and classroom discussion tool. Questions and explanations support review of the course concepts. All money shown in the challenge is fictional.
