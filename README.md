# Vocabulary + Punctuation Quiz

A self-contained vocabulary and punctuation practice quiz. Single HTML file — no build step, no dependencies beyond a browser.

**[Open the quiz](./vocab_punctuation_quiz.html)** *(once hosted, replace this with your actual GitHub Pages URL, e.g. `https://yourusername.github.io/vocab-quiz/vocab_punctuation_quiz.html`)*

---

## What it covers

- **468 words**, each testing both **definition recall** and **punctuation judgment** (identifying which of four marks — em dash, colon, semicolon, hyphen — correctly completes a sentence).
- **Weak-word tracking** that treats definition weakness and punctuation weakness as separate signals per word, so practice targets the specific gap rather than re-testing an already-mastered half.
- **Targeted practice by punctuation mark** — drill just semicolons, just hyphens, etc., directly from the progress screen.
- **Three word games**, all built from the same word list:
  - **Hangman** — guess the word from its definition.
  - **Spelling Bee** — find words from a 7-letter set (30+ puzzles, each guaranteed solvable). Words from your vocab list are bonus-highlighted when found. A **Hint** button reveals the definition of a random unfound vocab word for the current puzzle — since most puzzles only have one or two vocab words among their valid answers, hints can genuinely run out for a given puzzle, and the button says so plainly rather than failing silently. Found words are listed alphabetically.
  - **Mini crossword** — 30 puzzles, each a word crossed with several others at real shared letters, with reveal-letter and reveal-word hints available per clue.
- Word-of-the-day, a practice streak, and voice playback for pronunciation (where the browser supports it).

## Files it depends on

The core quiz works from `vocab_punctuation_quiz.html` alone. These additional files enable "Add to Home Screen" and offline access:

```
vocab_punctuation_quiz.html
vocab-manifest.json
vocab-service-worker.js
vocab-icon-192.png
vocab-icon-512.png
```

If the PWA files are missing, the quiz itself still works fully — only "Add to Home Screen" and offline mode won't be available.

## Progress data

Word stats, streak, and voice preference are all stored in the browser via `localStorage`, scoped to wherever the file is hosted. On GitHub Pages, that means progress persists reliably across visits to the same URL, unlike opening a local file directly, where storage can behave inconsistently depending on how the file was saved or reopened.

---

## Hosting on GitHub Pages — step by step

This uses GitHub's website only — no command line or git installation needed.

### 1. Create a GitHub account (skip if you already have one)
Go to [github.com](https://github.com) and sign up. It's free.

### 2. Create a new repository
1. Click the **+** icon in the top-right corner → **New repository**.
2. Give it a name, e.g. `vocab-quiz` (no spaces — use hyphens).
3. Set it to **Public** (required for free GitHub Pages hosting).
4. Leave everything else at its default, and click **Create repository**.

### 3. Upload the files
1. On your new repository's page, click **Add file → Upload files**.
2. Drag in every file listed above under "Files it depends on."
3. Scroll down and click **Commit changes**.

*(GitHub's upload page accepts multiple files at once — you don't need to do this one at a time. If you ever need to update a file later, use the same **Add file → Upload files** flow; uploading a file with the same name overwrites the old version.)*

### 4. Turn on GitHub Pages
1. In your repository, click **Settings** (top menu bar).
2. In the left sidebar, click **Pages**.
3. Under "Build and deployment," for **Source**, select **Deploy from a branch**.
4. Under "Branch," select **main** and **/ (root)**, then click **Save**.
5. Wait a minute or two — GitHub will show a message with your live URL once it's ready, in the form:
   `https://yourusername.github.io/vocab-quiz/`

### 5. Find your quiz
It's now live at:
`https://yourusername.github.io/vocab-quiz/vocab_punctuation_quiz.html`

(Replace `yourusername` and `vocab-quiz` with your actual GitHub username and whatever you named the repository.)

### 6. Bookmark it, or add it to your phone's home screen
Once live over HTTPS, the quiz supports "Add to Home Screen" on mobile for offline access — open the URL in your phone's browser, then use the browser's share/menu button to add it.

---

*No API keys, no backend, no build process — everything runs entirely in the browser.*
# Vocabulary + Punctuation Quiz

A self-contained vocabulary and punctuation practice quiz. Single HTML file — no build step, no dependencies beyond a browser.

**[Open the quiz](./vocab_punctuation_quiz.html)** *(once hosted, replace this with your actual GitHub Pages URL, e.g. `https://yourusername.github.io/vocab-quiz/vocab_punctuation_quiz.html`)*

---

## What it covers

- **468 words**, each testing both **definition recall** and **punctuation judgment** (identifying which of four marks — em dash, colon, semicolon, hyphen — correctly completes a sentence).
- **Weak-word tracking** that treats definition weakness and punctuation weakness as separate signals per word, so practice targets the specific gap rather than re-testing an already-mastered half.
- **Targeted practice by punctuation mark** — drill just semicolons, just hyphens, etc., directly from the progress screen.
- **Three word games**, all built from the same word list:
  - **Hangman** — guess the word from its definition.
  - **Spelling Bee** — find words from a 7-letter set (30+ puzzles, each guaranteed solvable). Words from your vocab list are bonus-highlighted when found. A **Hint** button reveals the definition of a random unfound vocab word for the current puzzle — since most puzzles only have one or two vocab words among their valid answers, hints can genuinely run out for a given puzzle, and the button says so plainly rather than failing silently. Found words are listed alphabetically.
  - **Mini crossword** — 30 puzzles, each a word crossed with several others at real shared letters, with reveal-letter and reveal-word hints available per clue.
- Word-of-the-day, a practice streak, and voice playback for pronunciation (where the browser supports it).

## Files it depends on

The core quiz works from `vocab_punctuation_quiz.html` alone. These additional files enable "Add to Home Screen" and offline access:

```
vocab_punctuation_quiz.html
vocab-manifest.json
vocab-service-worker.js
vocab-icon-192.png
vocab-icon-512.png
```

If the PWA files are missing, the quiz itself still works fully — only "Add to Home Screen" and offline mode won't be available.

## Progress data

Word stats, streak, and voice preference are all stored in the browser via `localStorage`, scoped to wherever the file is hosted. On GitHub Pages, that means progress persists reliably across visits to the same URL, unlike opening a local file directly, where storage can behave inconsistently depending on how the file was saved or reopened.

---

## Hosting on GitHub Pages — step by step

This uses GitHub's website only — no command line or git installation needed.

### 1. Create a GitHub account (skip if you already have one)
Go to [github.com](https://github.com) and sign up. It's free.

### 2. Create a new repository
1. Click the **+** icon in the top-right corner → **New repository**.
2. Give it a name, e.g. `vocab-quiz` (no spaces — use hyphens).
3. Set it to **Public** (required for free GitHub Pages hosting).
4. Leave everything else at its default, and click **Create repository**.

### 3. Upload the files
1. On your new repository's page, click **Add file → Upload files**.
2. Drag in every file listed above under "Files it depends on."
3. Scroll down and click **Commit changes**.

*(GitHub's upload page accepts multiple files at once — you don't need to do this one at a time. If you ever need to update a file later, use the same **Add file → Upload files** flow; uploading a file with the same name overwrites the old version.)*

### 4. Turn on GitHub Pages
1. In your repository, click **Settings** (top menu bar).
2. In the left sidebar, click **Pages**.
3. Under "Build and deployment," for **Source**, select **Deploy from a branch**.
4. Under "Branch," select **main** and **/ (root)**, then click **Save**.
5. Wait a minute or two — GitHub will show a message with your live URL once it's ready, in the form:
   `https://yourusername.github.io/vocab-quiz/`

### 5. Find your quiz
It's now live at:
`https://yourusername.github.io/vocab-quiz/vocab_punctuation_quiz.html`

(Replace `yourusername` and `vocab-quiz` with your actual GitHub username and whatever you named the repository.)

### 6. Bookmark it, or add it to your phone's home screen
Once live over HTTPS, the quiz supports "Add to Home Screen" on mobile for offline access — open the URL in your phone's browser, then use the browser's share/menu button to add it.

---

*No API keys, no backend, no build process — everything runs entirely in the browser.*
